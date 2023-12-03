Readline
========

Readline provides a Raku interface to libreadline.

Installation
------------

Please make sure that libreadline is installed beforehand, the tests will fail
otherwise. If libreadline is installed but the tests still fail, please note
that the Raku package searches a given set of directories for
libreadline.{so,dynlib}.* files, otherwise it defaults to v7. If your
libreadline installation isn't on any of these paths, or requires non-standard
setup, please file an issue.

For those of you on Linux Debian and Linux-alike systems, you should be able to
get the latest version with this CLI invocation:

``` sh
$ sudo apt-get install libreadline7
```

(I'd prefer to use LibraryCheck, but it fails inside the 'is native()' method
call.)

On macOS, use Hombrew or MacPorts to install readline. If you installed
Rakudo-Star with Homebrew after Sept. 1 it should already be there.

If not you can install just Readline

```  sh
brew install readline
```

or update your rakudo-star install.

``` sh
brew upgrade rakudo-star
```

Using zef (a module management tool bundled with Rakudo Star):

``` sh
$ zef update && zef install Readline
```

Or alternatively installing it from a checkout of this repo with zef:

``` sh
$ zef install .
```

Usage
-----

See the `examples/` directory in this project.

Testing
-------


To run tests:

``` sh
$ prove -e raku
```

Author
------

 - Jeffrey Goff, DrForr on #perl6, https://github.com/drforr/
 - Recently taken over by Daniel Lathrop (fooist), https://github.com/fooist/

License
-------

Artistic License 2.0
