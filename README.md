# birthday

![birthday](https://camo.githubusercontent.com/99ecb59d128268cd6d518befe9486f07733ade61/687474703a2f2f692e696d6775722e636f6d2f386a72397478442e706e67)

## About
Singularity recipe for [birthday](https://github.com/IonicaBizau/birthday#).

```
singularity inspect singularity-birthday.simg
{
    "WEBSITE": "http://www.cbd.cmu.edu/icaoberg",
    "org.label-schema.usage.singularity.deffile.bootstrap": "docker",
    "org.label-schema.usage.singularity.deffile": "Singularity",
    "AUTHOR": "icaoberg",
    "org.label-schema.schema-version": "1.0",
    "org.label-schema.usage.singularity.deffile.includecmd": "yes",
    "org.label-schema.build-size": "777MB",
    "org.label-schema.usage.singularity.deffile.from": "ubuntu:16.04",
    "org.label-schema.build-date": "Sun,_10_Feb_2019_22:17:15_-0500",
    "org.label-schema.usage.singularity.version": "2.6.0-dist",
    "EMAIL": "icaoberg@cmu.edu"
}
```

## Download
To download the image run the command

```
singularity pull --name birthday.simg shub://icaoberg/singularity-birthday
```

## Help
```
singularity run --app birthday singularity-birthday.simg --help
Usage: birthday [options]

Options:
  -n, --name <name>           The person name.
  -d, --date <date>           The person birthday or born date.
  -c, --coming <date>         Comming birthdays. Pass a date in the future.
  -b, --birthday-path <path>  Use a different birthday json file path.
  -h, --help                  Displays this help.
  -v, --version               Displays version information.

Examples:
  birthday -n 'Ionică Bizău' -d '14/09/1995'
  birthday -n 'Ionică Bizău' -d '14/09'
  birthday -c '2015-10-10'
  birthday # displays all birthdays

Documentation can be found at https://github.com/IonicaBizau/birthday
```

## Example
```
singularity run --app birthday singularity-birthday.simg -n "Albert Einstein" -d 04/01/1643
info  Inserted successfully

singularity run --app birthday singularity-birthday.simg -n "Isaac Newtown" -d 04/01/1643
info  Inserted successfully

singularity run --app birthday singularity-birthday.simg -n "Nikola Tesla" -d 07/10/1856
info  Inserted successfully

singularity run --app birthday singularity-birthday.simg
┌─┬───────────────┬───────────────┬───────────────┬───────────────┐
│#│Name           │Birthday       │Age            │               │
├─┼───────────────┼───────────────┼───────────────┼───────────────┤
│1│Albert Einstein│04 January     │376            │a month ago    │
├─┼───────────────┼───────────────┼───────────────┼───────────────┤
│2│Isaac Newtown  │04 January     │376            │a month ago    │
├─┼───────────────┼───────────────┼───────────────┼───────────────┤
│3│Nikola Tesla   │07 October     │162 → 163      │in 8 months    │
└─┴───────────────┴───────────────┴───────────────┴───────────────┘
```

---
[![CBD](http://www.cbd.cmu.edu/wp-content/uploads/2017/07/wordpress-default.png)](http://www.cbd.cmu.edu)

Copyleft © 2018-2019 [icaoberg](http://www.andrew.cmu.edu/~icaoberg) at the [Computational Biology Department](http://www.cbd.cmu.edu) in [Carnegie Mellon University](http://www.cmu.edu)
