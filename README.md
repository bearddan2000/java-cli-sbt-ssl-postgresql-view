# java-cli-sbt-ssl-postgresql-view

## Description
Creates a small database table
called `dog`. This table, `dog`, has been normalized to 3NF.
Two new tables have been added, `breedLookup` and `colorLookup`.

Creates a new table `dog_expanded` that joins
`dog`, `breedLookup` and `colorLookup`.

Added nonclustered indexes on
`dog`.breedId and `dog`.colorId. Turned `dog_expanded` into a view with an implicit index on `dog_expanded`.id.

Uses self-sign ssl.

## Tech stack
- java
- sbt
  - log4j
  - postgres driver

## Docker stack
- alpine:edge
- postgresql:alpine
- hseeberger/scala-sbt:11.0.2-oraclelinux7_1.3.5_2.12.10

## To run
`sudo ./install.sh -u`

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`
