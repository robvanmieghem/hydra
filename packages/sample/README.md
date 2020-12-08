# Sample Hydra Project

This is a sample project similar to the one generated by `hydra-cli scaffold`. By default, it runs against a
public [Kusama Indexer endpoint](https://indexer-kusama.joystream.app).

Experiment by modifying `schema.graphql` and the mapping files in the `mappings` folder.

## Codegen

Run

```bash
yarn codegen:all
```

to generate the model files as defined in `schema.graphql`

## DB Migrations

Inspect the DB settings in `.env` and prepare run the database migrations:

```bash
yarn db:prepare
yarn db:migrate
```

Note, that any schema changes in `schema.graphql` would require a fresh database. You may drop the old one by
running

```bash
yarn db:drop
```

## Run the processor and the GraphQL server

Then run the processor:

```bash
yarn processor:start
```

and the GraphQL server (opens a GraphQL playground at localhost by default):

```bash
yarn server:start:dev
```