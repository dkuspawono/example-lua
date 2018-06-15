[Codecov][1] Lua Example [![travisCI](https://travis-ci.org/codecov/example-lua.svg)](https://travis-ci.org/codecov/example-lua) [![codecov.io](http://codecov.io/github/codecov/example-lua/branch/master/graphs/badge.svg)](http://codecov.io/github/codecov/example-lua)
=====================

Note that the coverage is deliberately incomplete. (I swear by Kent Beck!) That
way you can [follow the badge link][5] and see how [Codecov][1] works. You can
view the code there, see hits and misses for coverage, etc.

## Guide
### Travis Setup

Add to your `.travis.yml` file.:fire:
```yml
language: c
after_success:
  - bash <(curl -s https://codecov.io/bash)
```
### Produce Coverage Reports  ***:rocket:***
Run your tests with [LuaCov][5] in order to create the necessary coverage
reports. For example:

```
lua -lluacov awesome-tests.lua
```
## Caveats
### Private Repos
Add to your `.travis.yml` file.
```yml
after_success:
  - bash <(curl -s https://codecov.io/bash) -t uuid-repo-token
```

1. More documentation at https://docs.codecov.io
2. Configure codecov through the `codecov.yml`  https://docs.codecov.io/docs/codecov-yaml

We are happy to help if you have any questions. Please contact email our Support at [support@codecov.io](mailto:support@codecov.io)

[1]: https://codecov.io/
[5]: http://keplerproject.github.io/luacov :white_check_mark:
