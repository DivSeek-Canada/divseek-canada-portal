# DivSeek Canada Portal

The [DivSeek Canada](http://www.divseekcanada.ca)  **Portal** is a web-based platform to implement association genetics 
workflows supporting plant breeding and crop research focusing on large scale plant genetic resources / crop 
genotype-phenotype data sets whose access is brokered / managed by the project.

# Genome Canada Pilot Project

The first iteration of the platform is funded under a 
[Genome Canada Project](https://www.genomecanada.ca/en/divseek-canada-harnessing-genomics-accelerate-crop-improvement-canada) with co-funding from other partners.

# Our Documentation

 - [Create DivSeek Canada Portal Guide](https://divseek-canada.github.io/divseek-canada-docs/en/latest/)

## Services:

Service                          | Address
-------------------------------- | ----
Galaxy                           | :8200
Tripal (/tripal)                 | :8200/tripal
Apollo (through Galaxy, /apollo) | :8200/apollo
Chado JBrowse Connector          | :8200/jbrowse/
PostgREST                        | :8200/postgrest
PostGraphQL Graph*i*QL interface | :8200/graphiql
PgAdmin4                         | :8201/
Chado PostGraphQL Connector      | :8200/jbrowse_graphql/

## Credentials

Service | Username         | Password
------- | ---------------- | ---------
Galaxy  | admin@galaxy.org | admin
Tripal  | admin            | changeme
Apollo  | admin@local.host | password

The Apollo account is only used internally by the Galaxy tools. You should be automatically logged in with your Galaxy account when connecting to Apollo (thanks to [gx-cookie-proxy](https://github.com/erasche/gx-cookie-proxy)).

## Dependencies

This `docker-compose.yml` depends on a large number of containers. We link some
build status images here for developer convenience

Image               | Status
-----               | ------
galaxy              | ![](https://quay.io/repository/galaxy-genome-annotation/docker-galaxy-annotation/status)
postgrest           | ![](https://quay.io/repository/erasche/postgrest/status)
postgraphql         | [![Docker Automated build](https://img.shields.io/docker/automated/erasche/postgraphql.svg?style=flat-square)](https://hub.docker.com/erasche/postgraphql)
chado-jb-connector  | ![](https://quay.io/repository/erasche/chado-jbrowse-connector/status)
chado               | ![](https://quay.io/repository/galaxy-genome-annotation/chado/status)
tripal              | ![](https://quay.io/repository/galaxy-genome-annotation/tripal/status)
gx-cookie-proxy     | ![](https://quay.io/repository/erasche/gx-cookie-proxy/status)

## Configuring

Each Docker image can be configured to fit your needs. You should consult the documentation of each image, in particular:

[Galaxy Docker image documentation](https://github.com/bgruening/docker-galaxy-stable)

[Tripal Docker image documentation](https://github.com/galaxy-genome-annotation/docker-tripal)

[Chado Docker image documentation](https://github.com/galaxy-genome-annotation/docker-chado)

[Apollo Docker image documentation](https://github.com/galaxy-genome-annotation/docker-apollo)

## LICENSE

GPLv3

## Support

This material is based upon work supported by the National Science Foundation under Grant Number (Award 1565146)
