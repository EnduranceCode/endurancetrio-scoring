# EnduranceTrio Scoring

**EnduranceTrio Scoring** is a web application that takes the data recorded by timing devices, such
as the ones produced by [MyLaps](https://www.mylaps.com/), and processes it to create and manage the
results of endurance races (*e.g.* running races and triathlons).

The development of this application is focused on the [MyLaps](https://www.mylaps.com/) timing
devices. When it becomes sufficient mature, it will then evolve to support other timing devices
brands.

## Development

The main tools and technologies used to develop this software
are [Git](https://git-scm.com/), [Maven](https://maven.apache.org/),
[MySQL](https://www.mysql.com/), [Java (JDK 11)](https://openjdk.org/projects/jdk/11/),
[Spring Boot](https://spring.io/) and [Thymeleaf](https://www.thymeleaf.org/).

To develop **EnduranceTrio Scoring** app start by cloning this repository with the following
command:

    git clone git@github.com:EnduranceCode/endurancetrio-scoring.git

**EnduranceTrio Scoring** uses [MySQL Server](https://www.mysql.com/) to manage its databases,
therefore, it has to
be [installed, configured and running](https://github.com/EnduranceCode/server-setup-guide/blob/master/03-mysql-server-installation.md)
in the development machine.

The file [`DATABASE.md`](./scoring-data/src/main/resources/db/DATABASE.md), stored in the
folder [`scoring-data/src/main/resources/db/`](./scoring-data/src/main/resources/db), documents the
process to create, upgrade and manage the databases needed to run the **EnduranceTrio Scoring** app.

## Deployment

### Database

**EnduranceTrio Scoring** uses [MySQL Server](https://www.mysql.com/) for its databases, therefore,
it has to be installed, configured and running in the server where the application is deployed.

The file [`DATABASE.md`](./scoring-data/src/main/resources/db/DATABASE.md), stored in the
folder [`scoring-data/src/main/resources/db/`](./scoring-data/src/main/resources/db), documents the
process to create, upgrade and manage the databases needed to run the **EnduranceTrio Scoring** app.

### Building

Prior to the build of the application, set the version on all `pom.xml` files, run the following
command:

    mvn versions:set -DnewVersion=VERSION_NUMBER

> VERSION_NUMBER : The new version number to be set on the pom.xml files

*Work in Progress*

## Usage

*Work in Progress*

## Licensing

The code in this project is [licensed](./LICENSE) under
the [MIT license](https://spdx.org/licenses/MIT.html).
