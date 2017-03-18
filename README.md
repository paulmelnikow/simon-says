simon-says
==========

A janky tool that makes it easier to keep your Travis build running.

This is currently in experimental state. When it matures a bit, I'll call it
stable. At that point, will make an effort to keep things backward-compatible.


Usage
-----

```yml
before_install:
  - test $CI && curl -sSL https://raw.githubusercontent.com/paulmelnikow/simon-says/master/simon-says -o simon-says && chmod +x simon-says
  - ./simon-says prepare
  - ./simon-says appledoc install
```


Motivation
----------

Super grateful to [Travis CI][], which is one of the only CI services
providing free OS X testing to open-source projects.

Keeping OS X builds running on Travis has unfortunately involved a bit of tail
chasing. Versions skew, tools fall in and out of compatibility with each
other, Xcode versions come and go.

Issue resolution sometimes takes a while, necessitating long-term workarounds:

https://github.com/travis-ci/travis-ci/issues/7031

Issues get fixed, and then regress:

https://github.com/travis-ci/travis-ci/issues/2183

Alternatives like gists don't have pull requests.

[Travis CI]: https://travis-ci.org/


License
-------

This project is licensed under the MIT License.
