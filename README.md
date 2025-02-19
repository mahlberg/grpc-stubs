gRPC Typing Stubs for Python
============================

This is a PEP-561-compliant stub-only package which provides type information of
[gRPC](https://grpc.io>).

Install using pip:

    pip install grpc-stubs


Tests (courtesy of [pytest-mypy-plugins](https://github.com/typeddjango/pytest-mypy-plugins>):

    pip install -r requirements-dev.txt
    ./tools.sh test


## Python Support

grpc-stubs is tested with 3.7 or later, but ideally it should support Python 3.6 as
grpc still supports this. Python 3.6 had to be disabled in the tests due to
various cascading fiascos and a lack of time to contend with them. Feel free
to submit a PR if you'd like to see it returned, or open issues. Ensure that
you supply an MRE as per the contributing guidelines below.


## Contributing

### Minimum Reproducible Examples (MRE)

Unfortunately, due to the fussy nature of `grpc` and its dependencies, and the huge amount of time
required to construct a context in which to verify and debug issues, starting from 2022-04-16, fairly strict issue and
pull request templates have been added.

Minimum Reproducible Examples are now a hard requirement for pull requests that touch the typing surface,
and a soft requirement for issues. PRs without a functioning MRE transfer the burden entirely from the
contributor to the maintainer, and I simply don't have time to do the deep-dives required to build out MREs
from scratch when issues inevitably crop up. PRs without a trivially executable MRE will be closed without further
consideration; of course you are always welcome to reopen once you have added a verified MRE!


### Tests

This project uses a slightly old version of https://github.com/TypedDjango/pytest-mypy-plugins for testing.
All new contributions will be required to include at least one, but probably multiple tests. See
`typesafety/test_*.yml`.


### Code-generated stubs

PRs containing auto-generated stubs have had to be reverted several times due to issues. Starting
from 2022-04-16, autogenerated stubs from `mypy-protobuf` will not be accepted without extensive
tests, and will not be accepted with edit warnings left in. It's ok to use this tool to seed stubs,
but not to refresh stubs - once contributed to this repo, the stubs should be presumed to have been
written by hand.


## Calls for assistance

There are several areas where `grpc-stubs` could use some TLC. If you'd like to help with any
of this, please reach out!


### Maintainers

It's unlikely I'll be returning to grpc full-time for the foreseeable future, and my knowledge of the
minutiae fades with each passing year. If anyone wishes to assume maintainership of this project ongoing,
please reach out.


## Other Very Useful Typed Python Stuff

- https://github.com/TypedDjango
- https://github.com/typeddjango/pytest-mypy-plugins
- https://github.com/typeddjango/awesome-python-stubs

