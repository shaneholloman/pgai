# Chunk text with SQL functions

The `ai.chunk_text` and `ai.chunk_text_recursively` functions allow you to split text into smaller chunks.

## Example usage

Given a table like this

```sql
create table blog
( id int not null primary key
, title text
, body text
);
```

You can chunk the text in the `body` column like this

```sql
select
  b.id
, b.title
, c.seq
, c.chunk
from blog b
cross join lateral ai.chunk_text(b.body) c
order by b.id, c.seq
;
```

## chunk_text

Splits text into chunks using a separator. 
This uses the [CharacterTextSplitter](https://python.langchain.com/api_reference/text_splitters/character/langchain_text_splitters.character.CharacterTextSplitter.html) from the `langchain_text_splitters` Python package.

| Name                | Type  | Default  | Required | Description                                               |
|---------------------|-------|----------|----------|-----------------------------------------------------------|
| input               | text  | -        | ✔        | The text to split into chunks                             |
| chunk_size          | int   | *4000    | ✖        | The target size of a chunk in characters                  |
| chunk_overlap       | int   | *200     | ✖        | The target amount of overlapping characters in each chunk |
| separator           | text  | *E'\n\n' | ✖        | The text to split on                                      |
| is_separator_regex  | text  | false    | ✖        | `true` if the separator represents a regular expression   |
*defaulted by the underlying Python implementation rather than in SQL

```sql
select *
from ai.chunk_text
($$if two witches watch two watches, which witch watches which watch?$$
, separator=>' '
, chunk_size=>10
, chunk_overlap=>0
);
```
The query above will return the results below:
```
 seq |   chunk
-----+-----------
   0 | if two
   1 | witches
   2 | watch two
   3 | watches,
   4 | which
   5 | witch
   6 | watches
   7 | which
   8 | watch?
(9 rows)
```


## chunk_text_recursively

Recursively splits text into chunks using multiple separators in sequence.
This uses the [RecursiveCharacterTextSplitter](https://python.langchain.com/api_reference/text_splitters/character/langchain_text_splitters.character.RecursiveCharacterTextSplitter.html) from the `langchain_text_splitters` Python package.

| Name               | Type   | Default                         | Required | Description                                               |
|--------------------|--------|---------------------------------|----------|-----------------------------------------------------------|
| input              | text   | -                               | ✔        | The text to split into chunks                             |
| chunk_size         | int    | *4000                           | ✖        | The target size of a chunk in characters                  |
| chunk_overlap      | int    | *200                            | ✖        | The target amount of overlapping characters in each chunk |
| separators         | text[] | *array[E'\n\n', E'\n', ' ', ''] | ✖        | An array of texts to split on                             |
| is_separator_regex | text   | false                           | ✖        | `true` if the separators represents regular expressions   |
*defaulted by the underlying Python implementation rather than in SQL

```sql
select *
from ai.chunk_text_recursively
($$if two witches watch two watches, which witch watches which watch?$$
, separators=>array[' ', '.', '?']
, chunk_size=>2
, chunk_overlap=>0
);
```
The query above will return the results below:
```
 seq |   chunk
-----+-----------
   0 | if
   1 |  two
   2 |  witches
   3 |  watch
   4 |  two
   5 |  watches,
   6 |  which
   7 |  witch
   8 |  watches
   9 |  which
  10 |  watch
  11 | ?
(12 rows)
```