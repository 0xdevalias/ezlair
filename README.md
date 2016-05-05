# ezLair

ezLair makes setting up and running the [Lair Framework](https://github.com/lair-framework) easy!

Note: This is a WIP, [YMMV](https://en.wiktionary.org/wiki/YMMV). (I'd like to clean this up a bunch but.. done is better than perfect)

## Getting Started

* Current assumptions:
  * You're setting this up in `~/sec/ezlair`
  * You have the [docker native beta](https://blog.docker.com/2016/03/docker-for-mac-windows-beta/) installed (or a version that can [handle volume mounts with mongo](https://docs.mongodb.org/manual/administration/production-notes/#fsync-on-directories), tested on `v1.11.1`)
    * The `ezlair-mongo-*` and `ezlair` scripts require this.
    * Could work around this with a local mongo install.
  * You're running on OSX
    * Workaround: Hack some of the scripts to set the version to your platform (notably `ezlair-download` and `ezlair-api-start`)
  * You have `python` installed (currently only required for `ezlair-download`, tested against 2.x)
  * You have `tmux` installed (only used by the main `ezlair` script)
    * Workaround: Run `ezlair-app-start` and `ezlair-api-start` manually.
  * You have [nodenv](https://github.com/nodenv/nodenv) installed with `node-build` (used by `ezlair-app-start`), or your default node version is `v0.10.40`
* If you're ok with all of that:
  * `git clone git@github.com:alias1/ezlair.git`
  * `cd ezlair`
  * `./ezlair-download`
  * `./ezlair-mongo-create`
  * `./ezlair`
    * Note: This will generate an admin user with a random password the first time it's run. Make sure to make note of it.

## Wiping data

* Resetting the database
  * `./ezlair-mongo-reset`
  * `./ezlair-mongo-create`
* Wipe it all
  * `./ezlair-cleanup`

## What is the Lair Framework?

From the [project page](https://github.com/lair-framework):
> Lair is a reactive attack collaboration framework and web application built with meteor.

## Who made ezLair?

* Glenn 'devalias' Grant
  * http://www.devalias.net/
  * [@_devalias](https://twitter.com/_devalias)

## License

See the [LICENSE](https://github.com/alias1/ezlair/blob/master/LICENSE) file.