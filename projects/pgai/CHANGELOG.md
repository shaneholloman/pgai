# Changelog

## [0.6.0](https://github.com/shaneholloman/pgai/compare/pgai-v0.5.0...pgai-v0.6.0) (2025-01-25)


### ⚠ BREAKING CHANGES

* remove `truncate` parameter from Ollama/Voyage APIs ([#284](https://github.com/shaneholloman/pgai/issues/284))

### Features

* add alembic operations for vectorizer ([#266](https://github.com/shaneholloman/pgai/issues/266)) ([b01acfe](https://github.com/shaneholloman/pgai/commit/b01acfeeb7f0472de0337442c3c63a51d6690167))
* add LiteLLM vectorizer integration ([0fb7e46](https://github.com/shaneholloman/pgai/commit/0fb7e46b9eb1f69b0fb67c6a67ff5bf9e96c0cf3))
* add Ollama support to vectorizer ([6a4a449](https://github.com/shaneholloman/pgai/commit/6a4a449e99e2e5e62b5f551206a0b28e5ad40802))
* add sqlalchemy vectorizer_relationship ([#265](https://github.com/shaneholloman/pgai/issues/265)) ([0230509](https://github.com/shaneholloman/pgai/commit/0230509a374c472d65280769f92f0baeebb908d7))
* add Voyage AI vectorizer integration ([#256](https://github.com/shaneholloman/pgai/issues/256)) ([1b56d62](https://github.com/shaneholloman/pgai/commit/1b56d62295faf996697db75f3a9ac9391869a3bb))
* allow users to configure a base_url for the vectorizer OpenAI embedder ([#351](https://github.com/shaneholloman/pgai/issues/351)) ([66ceb3d](https://github.com/shaneholloman/pgai/commit/66ceb3dc62712b82f45e2485072595c2f402065b))
* load api keys from db in self hosted vectorizer ([#311](https://github.com/shaneholloman/pgai/issues/311)) ([b7573b7](https://github.com/shaneholloman/pgai/commit/b7573b79711a691a37201e06f6e5ba52631b69b9))
* print unexpected error traceback in debug logs ([#344](https://github.com/shaneholloman/pgai/issues/344)) ([d9bdcd6](https://github.com/shaneholloman/pgai/commit/d9bdcd633fe372fca14dd97d830aeed9789f78ac))
* pull missing ollama models ([#301](https://github.com/shaneholloman/pgai/issues/301)) ([dbac246](https://github.com/shaneholloman/pgai/commit/dbac246b563f10d1704b40bf16038b16529d6888))
* remove `truncate` parameter from Ollama/Voyage APIs ([#284](https://github.com/shaneholloman/pgai/issues/284)) ([ecda03c](https://github.com/shaneholloman/pgai/commit/ecda03cf5d27f750db534801719413d0abcfa557))
* upgrade ollama client to 0.4.5 ([#345](https://github.com/shaneholloman/pgai/issues/345)) ([c579238](https://github.com/shaneholloman/pgai/commit/c57923804532980d8b2bb5e3b47a927c48f55df0))


### Bug Fixes

* fail fast when api key is missing and once is set ([#274](https://github.com/shaneholloman/pgai/issues/274)) ([1c2ff20](https://github.com/shaneholloman/pgai/commit/1c2ff2013fd64949a8f5c6374e3134af1b2551f4))
* handle 'null' value in chunking 'chunk_column' ([#340](https://github.com/shaneholloman/pgai/issues/340)) ([f283b6c](https://github.com/shaneholloman/pgai/commit/f283b6cecd7da42a5197da6219b990598e19f9f0))
* make vectorizer worker poll for new vectorizers ([0672e7a](https://github.com/shaneholloman/pgai/commit/0672e7a71e2792c984ce9a590a06de9bfd25c8b5))
* make vectorizer worker robust ([#263](https://github.com/shaneholloman/pgai/issues/263)) ([77c0baf](https://github.com/shaneholloman/pgai/commit/77c0baf57438a837f47c179769bc684edeafbfc8))
* two usability issues with sqlalchemy ([#354](https://github.com/shaneholloman/pgai/issues/354)) ([95fa797](https://github.com/shaneholloman/pgai/commit/95fa797f559adfbaf91ff5198db0d7c45381e1dc))
* vectorizer_relationship for sqlalchemy models with mixins or inheritance ([#357](https://github.com/shaneholloman/pgai/issues/357)) ([cfd5f73](https://github.com/shaneholloman/pgai/commit/cfd5f73606e1a6b88eab00d043bded8d898ab4dd))


### Miscellaneous

* a new database for each test ([4ed938b](https://github.com/shaneholloman/pgai/commit/4ed938bd86932bf21340e14007210d8dc6fd72e1))
* add logo to pgai pypi ([3366368](https://github.com/shaneholloman/pgai/commit/336636872b39ce371d801f4ffacd1ea57e67b9f5))
* add test for recursive text splitting ([#207](https://github.com/shaneholloman/pgai/issues/207)) ([4a35fc6](https://github.com/shaneholloman/pgai/commit/4a35fc693395bc4125b9654650043cad5929889e))
* fix broken pgai build by pinning hatchling ([#308](https://github.com/shaneholloman/pgai/issues/308)) ([5441f2d](https://github.com/shaneholloman/pgai/commit/5441f2d3445b1f2afc85ce34b220002b8e4cf08f))
* **main:** release pgai 0.2.0 ([a42d3e5](https://github.com/shaneholloman/pgai/commit/a42d3e59652b7adbd4a688f0e099f647f14f0901))
* **main:** release pgai 0.2.1 ([3526907](https://github.com/shaneholloman/pgai/commit/3526907940f91b87a9f24a25460d16be398598af))
* **main:** release pgai 0.3.0 ([#277](https://github.com/shaneholloman/pgai/issues/277)) ([0146781](https://github.com/shaneholloman/pgai/commit/0146781f4ba641ae78fd5943a5fbb6997519c1a5))
* **main:** release pgai 0.4.0 ([a41d7b4](https://github.com/shaneholloman/pgai/commit/a41d7b4f2dd4c2cff03d5882762b37d92b405f43))
* **main:** release pgai 0.5.0 ([#355](https://github.com/shaneholloman/pgai/issues/355)) ([fb02a19](https://github.com/shaneholloman/pgai/commit/fb02a19ea03debec7d7fbf7bdce3e3603b078292))
* migrate project commands from Make to Just ([42a8f79](https://github.com/shaneholloman/pgai/commit/42a8f795c89bfc7526008dda7c99a3d6a4ecce70))
* migrate to uv and hatch ([#188](https://github.com/shaneholloman/pgai/issues/188)) ([627cf33](https://github.com/shaneholloman/pgai/commit/627cf33e802cac01f2a204aecf994ceb9509a84e))
* refactor test infra ([ac845ca](https://github.com/shaneholloman/pgai/commit/ac845ca8dc834e0359113fd63d30c6ec98e041a7))
* register postgres_params custom pytest.mark ([#327](https://github.com/shaneholloman/pgai/issues/327)) ([89039b2](https://github.com/shaneholloman/pgai/commit/89039b2181192191dad48dc8206e76b17643e129))
* run pgai tests against extension from source ([ffc20d2](https://github.com/shaneholloman/pgai/commit/ffc20d243c2a632d01c5e3476ddbc6c636d994c1))
* scope postgres_container fixture to class ([12c1780](https://github.com/shaneholloman/pgai/commit/12c17809ec235d759e37eaa0898ea3274fea6319))
* separate the dev/test/build between the projects ([183be9e](https://github.com/shaneholloman/pgai/commit/183be9e82632287c35081c4eefd81ff99d4bd4ba))
* split embedders in individual files ([#315](https://github.com/shaneholloman/pgai/issues/315)) ([77673ee](https://github.com/shaneholloman/pgai/commit/77673eee81191c7f2c8966010fe8f04d9a929dee))
* test the cli instead of the lambda handler ([#204](https://github.com/shaneholloman/pgai/issues/204)) ([3a48f82](https://github.com/shaneholloman/pgai/commit/3a48f82b103175b83d1036bff31b00f5122606aa))

## [0.5.0](https://github.com/timescale/pgai/compare/pgai-v0.4.0...pgai-v0.5.0) (2025-01-22)


### Features

* add alembic operations for vectorizer ([#266](https://github.com/timescale/pgai/issues/266)) ([b01acfe](https://github.com/timescale/pgai/commit/b01acfeeb7f0472de0337442c3c63a51d6690167))
* allow users to configure a base_url for the vectorizer OpenAI embedder ([#351](https://github.com/timescale/pgai/issues/351)) ([66ceb3d](https://github.com/timescale/pgai/commit/66ceb3dc62712b82f45e2485072595c2f402065b))


### Bug Fixes

* two usability issues with sqlalchemy ([#354](https://github.com/timescale/pgai/issues/354)) ([95fa797](https://github.com/timescale/pgai/commit/95fa797f559adfbaf91ff5198db0d7c45381e1dc))
* vectorizer_relationship for sqlalchemy models with mixins or inheritance ([#357](https://github.com/timescale/pgai/issues/357)) ([cfd5f73](https://github.com/timescale/pgai/commit/cfd5f73606e1a6b88eab00d043bded8d898ab4dd))

## [0.4.0](https://github.com/timescale/pgai/compare/pgai-v0.3.0...pgai-v0.4.0) (2025-01-08)


### Features

* add sqlalchemy vectorizer_relationship ([#265](https://github.com/timescale/pgai/issues/265)) ([0230509](https://github.com/timescale/pgai/commit/0230509a374c472d65280769f92f0baeebb908d7))
* load api keys from db in self hosted vectorizer ([#311](https://github.com/timescale/pgai/issues/311)) ([b7573b7](https://github.com/timescale/pgai/commit/b7573b79711a691a37201e06f6e5ba52631b69b9))
* print unexpected error traceback in debug logs ([#344](https://github.com/timescale/pgai/issues/344)) ([d9bdcd6](https://github.com/timescale/pgai/commit/d9bdcd633fe372fca14dd97d830aeed9789f78ac))
* pull missing ollama models ([#301](https://github.com/timescale/pgai/issues/301)) ([dbac246](https://github.com/timescale/pgai/commit/dbac246b563f10d1704b40bf16038b16529d6888))
* upgrade ollama client to 0.4.5 ([#345](https://github.com/timescale/pgai/issues/345)) ([c579238](https://github.com/timescale/pgai/commit/c57923804532980d8b2bb5e3b47a927c48f55df0))


### Bug Fixes

* handle 'null' value in chunking 'chunk_column' ([#340](https://github.com/timescale/pgai/issues/340)) ([f283b6c](https://github.com/timescale/pgai/commit/f283b6cecd7da42a5197da6219b990598e19f9f0))


### Miscellaneous

* fix broken pgai build by pinning hatchling ([#308](https://github.com/timescale/pgai/issues/308)) ([5441f2d](https://github.com/timescale/pgai/commit/5441f2d3445b1f2afc85ce34b220002b8e4cf08f))
* register postgres_params custom pytest.mark ([#327](https://github.com/timescale/pgai/issues/327)) ([89039b2](https://github.com/timescale/pgai/commit/89039b2181192191dad48dc8206e76b17643e129))
* split embedders in individual files ([#315](https://github.com/timescale/pgai/issues/315)) ([77673ee](https://github.com/timescale/pgai/commit/77673eee81191c7f2c8966010fe8f04d9a929dee))

## [0.3.0](https://github.com/timescale/pgai/compare/pgai-v0.2.1...pgai-v0.3.0) (2024-12-10)


### ⚠ BREAKING CHANGES

* remove `truncate` parameter from Ollama/Voyage APIs ([#284](https://github.com/timescale/pgai/issues/284))

### Features

* add Voyage AI vectorizer integration ([#256](https://github.com/timescale/pgai/issues/256)) ([1b56d62](https://github.com/timescale/pgai/commit/1b56d62295faf996697db75f3a9ac9391869a3bb))
* remove `truncate` parameter from Ollama/Voyage APIs ([#284](https://github.com/timescale/pgai/issues/284)) ([ecda03c](https://github.com/timescale/pgai/commit/ecda03cf5d27f750db534801719413d0abcfa557))


### Bug Fixes

* fail fast when api key is missing and once is set ([#274](https://github.com/timescale/pgai/issues/274)) ([1c2ff20](https://github.com/timescale/pgai/commit/1c2ff2013fd64949a8f5c6374e3134af1b2551f4))

## [0.2.1](https://github.com/timescale/pgai/compare/pgai-v0.2.0...pgai-v0.2.1) (2024-12-02)


### Bug Fixes

* make vectorizer worker robust ([#263](https://github.com/timescale/pgai/issues/263)) ([77c0baf](https://github.com/timescale/pgai/commit/77c0baf57438a837f47c179769bc684edeafbfc8))

## [0.2.0](https://github.com/timescale/pgai/compare/pgai-v0.1.0...pgai-v0.2.0) (2024-11-26)


### Features

* add Ollama support to vectorizer ([6a4a449](https://github.com/timescale/pgai/commit/6a4a449e99e2e5e62b5f551206a0b28e5ad40802))


### Bug Fixes

* make vectorizer worker poll for new vectorizers ([0672e7a](https://github.com/timescale/pgai/commit/0672e7a71e2792c984ce9a590a06de9bfd25c8b5))


### Miscellaneous

* a new database for each test ([4ed938b](https://github.com/timescale/pgai/commit/4ed938bd86932bf21340e14007210d8dc6fd72e1))
* add logo to pgai pypi ([3366368](https://github.com/timescale/pgai/commit/336636872b39ce371d801f4ffacd1ea57e67b9f5))
* add test for recursive text splitting ([#207](https://github.com/timescale/pgai/issues/207)) ([4a35fc6](https://github.com/timescale/pgai/commit/4a35fc693395bc4125b9654650043cad5929889e))
* migrate project commands from Make to Just ([42a8f79](https://github.com/timescale/pgai/commit/42a8f795c89bfc7526008dda7c99a3d6a4ecce70))
* migrate to uv and hatch ([#188](https://github.com/timescale/pgai/issues/188)) ([627cf33](https://github.com/timescale/pgai/commit/627cf33e802cac01f2a204aecf994ceb9509a84e))
* refactor test infra ([ac845ca](https://github.com/timescale/pgai/commit/ac845ca8dc834e0359113fd63d30c6ec98e041a7))
* run pgai tests against extension from source ([ffc20d2](https://github.com/timescale/pgai/commit/ffc20d243c2a632d01c5e3476ddbc6c636d994c1))
* scope postgres_container fixture to class ([12c1780](https://github.com/timescale/pgai/commit/12c17809ec235d759e37eaa0898ea3274fea6319))
* separate the dev/test/build between the projects ([183be9e](https://github.com/timescale/pgai/commit/183be9e82632287c35081c4eefd81ff99d4bd4ba))
* test the cli instead of the lambda handler ([#204](https://github.com/timescale/pgai/issues/204)) ([3a48f82](https://github.com/timescale/pgai/commit/3a48f82b103175b83d1036bff31b00f5122606aa))
