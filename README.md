# libmemcached

[![Gitter Badge]](https://gitter.im/m6w6/libmemcached)
[![License Badge]](https://opensource.org/licenses/BSD-3-Clause)

[Gitter Badge]:     https://badges.gitter.im/m6w6/libmemcached.svg "Gitter Chat"
[License Badge]:    https://img.shields.io/badge/License-BSD%203--Clause-blue.svg "BSD 3-Clause"

libmemcached is an open source C/C++ client library and tools for the
memcached server (http://memcached.org/). It has been designed to be
light on memory usage, thread safe, and provide full access to server
side methods.

> **NOTE:**  
> This is a resurrection of the original work from Brian Aker at
> [libmemcached.org](https://libmemcached.org) and the only publicly maintained
> version of libmemcached currently known to me.

## Documentation

[![Docs Actions Badge]](
    https://github.com/m6w6/libmemcached/actions?query=workflow%3Adocs-publish-pages)

[Docs Actions Badge]:
    https://github.com/m6w6/libmemcached/workflows/docs-publish-pages/badge.svg?branch=v1.x
    "Github Docs Action"

See https://m6w6.github.io/libmemcached

### Building and updating docs

See [gh-pages/publish](./docs/gh-pages/publish.sh) script and the
[docs-publish-pages](./.github/workflows/docs-publish-pages.yml) workflow,
which automate pushing updated documentation to github pages.

## Installing

libmemcached uses `CMake`.
Please see/edit [`CMakeConfig.txt`](./CMakeConfig.txt) or use `ccmake(1)` to
set any preferred options.

### From source

    git clone github.com:m6w6/libmemcached
    mkdir build-libmemcached
    cd $_
    cmake ../libmemcached
    make
    sudo make install

## Testing

[![Codecov Badge]](https://codecov.io/gh/m6w6/libmemcached)

[Codecov Badge]:
    https://codecov.io/gh/m6w6/libmemcached/branch/v1.x/graph/badge.svg
    "Code coverage"

Enable the `BUILD_TESTING` setting for a build and run `make test`.

    cmake -DBUILD_TESTING=ON ../libmemcached
    make test

### Continuous integration

[![Travis Badge]](https://travis-ci.org/github/m6w6/libmemcached)
[![Actions Badge]](https://github.com/m6w6/libmemcached/actions?query=workflow%3Acmake-build-ci)
[![Sourcehut Badge]](https://builds.sr.ht/~m6w6/libmemcached)

[Travis Badge]:
    https://api.travis-ci.org/m6w6/libmemcached.svg?branch=v1.x
    "Travis CI"
[Actions Badge]:
    https://github.com/m6w6/libmemcached/workflows/cmake-build-ci/badge.svg?branch=v1.x
    "Github Actions"
[Sourcehut Badge]:
    https://builds.sr.ht/~m6w6/libmemcached/commits.svg
    "Sourcehut Builds"

CI/Test results are performed on the follwing system matrix:

| OS               | Compiler                     | Arch                  |
|------------------|------------------------------|-----------------------|
| Linux            | GNU 9                        | arm64, ppc64le, s390x |
| Linux            | GNU 7/8/9/10, Clang 6/8/9/10 | amd64                 |
| MacOS            | Clang 12 (apple)             | amd64                 |
| FreeBSD, OpenBSD | Clang 8                      | amd64                 |

libmemcached has been tested against [memcached](https://github.com/memcached/memcached) v1.5 and v1.6.

## ChangeLog

Check out the latest [releases](https://github.com/m6w6/libmemcached/releases)
or the bundled [ChangeLog](./ChangeLog.md) for a comprehensive list of changes.

## License

libmemcached is licensed under the 3-Clause-BSD license, which can be
found in the accompanying [LICENSE](./LICENSE) file.

## Contributing

Please report any issues on the [bug tracker](https://github.com/m6w6/libmemcached/issues).

A list of known permanent issues is maintained in [BUGS](./BUGS.md).

All forms of contribution are welcome! Please see the bundled
[CONTRIBUTING](./CONTRIBUTING.md) note for the general principles followed.

The list of current and past maintainers and contributors is available in [AUTHORS](./AUTHORS).

