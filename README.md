# hub Snap Package [![CircleCI Build Status](https://circleci.com/gh/felicianotech/hub-snap.svg?style=shield)](https://circleci.com/gh/felicianotech/hub-snap) [![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/felicianotech/hub-snap/master/LICENSE)

`hub` is a command-line tool that wraps Git in order to extend it with extra features and commands that make working with GitHub easier.
This repository provides the source code for the `hub` snap which is available in the [Snapcraft Store](https://snapcraft.io/hub).
The snap is maintained by [@FelicianoTech](https://twitter.com/FelicianoTech) meanwhile the code for `hub` itself is maintained by GitHub.
The upstream repository can be found [here](https://github.com/github/hub).


## Installation

`hub` can be installed via snap on Ubuntu 16.04, Ubuntu 18.04+, and many Linux distros with `snapd` installed  by running:

```
sudo snap install --classic hub
```

If you don't have the `snap` command available, you might be able to find instructions for your distro [here](https://docs.snapcraft.io/core/install).
All other install methods can be found [here](https://github.com/github/hub#installation).


## Usage

You can run any Git command via hub simply by swapping out `git` for `hub` in the command.
In fact, it is suggested to alias `git` to run `hub` instead.

Convenient commands such as `hub clone felicianotech/hub-snap` could be run instead of the longer `git clone git://github.com/felicianotech/hub-snap.git`.
A full list of commands can be found in hub's [user manual](https://hub.github.com/hub.1.html).


## Development

This snap can be built with Snapcraft.
On Ubuntu:


```
sudo snap install --classic snapcraft
snapcraft snap
```

Originally this snap was suppose to simply package the binaries already published by GitHub.
Problem is, the binaries they make aren't statically linked which makes the snap world difficult.
So instead, we're compiling `hub` based off the appropriate Git tag.


## License

Both the code for this snap as well as `hub` itself is licensed under the MIT license.
This repo's license can be found [here](./LICENSE) while the license for `hub` can be found [here](https://github.com/github/hub/blob/master/LICENSE).
