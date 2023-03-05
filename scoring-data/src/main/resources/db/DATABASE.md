# EnduranceTrio Scoring

This file documents the process to create, upgrade and manage the databases needed to run
the [EnduranceTrio Scoring](https://github.com/EnduranceCode/endurancetrio-scoring) app.

## Application Databases

To enable **EnduranceTrio Scoring** app to access the timing data recorded by
the [MyLaps](https://www.mylaps.com/) devices, a databases managed by **EnduranceTrio** must be
added as an *exporter* of
the [Timing & Scoring Software](https://www.mylaps.com/timing-scoring-software/).

As a safety measure, the **EnduranceTrio Scoring** app will manage two different databases: one for
its data and another that is exclusively used to receive the data
from [Timing & Scoring Software](https://www.mylaps.com/timing-scoring-software/). This database is
the `endurancetrio_mylaps` database. The user `mylaps-user` is the one that will be used
by [Timing & Scoring software](https://www.mylaps.com/timing-scoring-software/) to export its data,
and it has the minimum possible access level to the database.

## Database Scripts

The scripts necessary to create and migrate the databases used by the
***EnduranceTrio Scoring*** app are stored in the sub-folders of this folder. The scripts necessary
to create the databases are stored in the folder [creation](./creation) and the scripts necessary to
migrate the databases are stored in the folder [migration](./migration).

The scripts must be executed following its names alphabetical order, starting with the scripts
inside the [creation](./creation) and then moving to the scripts stored in
the [migration](./migration) folder.

The scripts must respect the following naming convention (which is compatible with
the [Flyway](https://www.red-gate.com/products/flyway/) naming patterns:

    Vxxx.yyy.zzz.nnn__free-description.sql

> ***xxx*** : Major version number at the time of the script creation
>
> ***yyy*** : Minor version number at the time of the script creation
>
> ***zzz*** : Patch version number at the time of the script creation
>
> ***nnn*** : Order number for version number at the time of the script creation
>
> ***free_description*** : A short free description of the scripts actions with words separated with
> dashes 

