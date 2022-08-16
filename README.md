# Milvus Python SDK

[![version](https://img.shields.io/pypi/v/pymilvus.svg?color=blue)](https://pypi.org/project/pymilvus/)
[![Supported Python Versions](https://img.shields.io/pypi/pyversions/pymilvus?logo=python&logoColor=blue)](https://pypi.org/project/pymilvus/)
[![Downloads](https://pepy.tech/badge/pymilvus)](https://pepy.tech/project/pymilvus)
[![Downloads](https://pepy.tech/badge/pymilvus/month)](https://pepy.tech/project/pymilvus/month)
[![Downloads](https://pepy.tech/badge/pymilvus/week)](https://pepy.tech/project/pymilvus/week)
[![license](https://img.shields.io/hexpm/l/plug.svg?color=green)](https://github.com/milvus-io/pymilvus/blob/master/LICENSE)
[![Mergify Status][mergify-status]][mergify]


Python SDK for [Milvus](https://github.com/milvus-io/milvus). To contribute code to this project, please read our [contribution guidelines](https://github.com/milvus-io/milvus/blob/master/CONTRIBUTING.md) first. If you have some ideas or encounter a problem, you can find us in the Slack channel [#py-milvus](https://milvusio.slack.com/archives/C024XTWMT4L).


## Compatibility
The following collection shows Milvus versions and recommended PyMilvus versions:

|Milvus version| Recommended PyMilvus version |
|:-----:|:-----:|
| 1.0.* | 1.0.1 |
| 1.1.* | 1.1.2 |
| 2.0.* | 2.0.2 |
| 2.1.* | 2.1.1 |


## Installation

You can install PyMilvus via `pip` or `pip3` for Python 3.6+:

```shell
$ pip3 install pymilvus
```

You can install a specific version of PyMilvus by:

```shell
$ pip3 install pymilvus==2.1.1
```

You can upgrade PyMilvus to the latest version by:

```shell
$ pip3 install --upgrade pymilvus
```

## FAQ
Q1. How to get submodules?

A1. The following command will get the protos matching to the generated files, for protos of certain version, see
[milvus-proto](https://github.com/milvus-io/milvus-proto#usage) for details.
```shell
$ git submodule update --init
```

Q2. How to generate python files from milvus-proto?

**Before generating python files, please install requirements in `requirements.txt`**

A2.
```shell
$ make gen_proto
```

Q3. How to use the local PyMilvus repository for Milvus server?

A3.
```shell
$ python setup.py install
```


## Documentation

Documentation is available online: https://milvus.io/api-reference/pymilvus/v2.1.1/install.html.


## Developing package releases

The commits on the development branch of each version will be packaged and uploaded to [Test PyPI](https://test.pypi.org/).

The package name generated by the development branch is x.y.z.dev<dist>, where <dist> is the number of commits that differ from the most recent release.

- For example, after the release of 2.0.1, two commits were submitted on the 2.0 branch.
The version number of the latest commit of 2.0 branch is **2.0.2.dev2**.

- For example, after the release of 2.0.1, 10 commits were submitted on the master branch.
The version number of the latest commit of master branch is **2.1.0.dev10**.


To install the package on Test PyPi, you need to append `--extra-index-url` after pip, for example:
```shell
$ python3 -m pip install --extra-index-url https://test.pypi.org/simple/ pymilvus==2.1.0.dev66
```


## License
[Apache License 2.0](LICENSE)


[mergify]: https://mergify.io
[mergify-status]: https://img.shields.io/endpoint.svg?url=https://gh.mergify.io/badges/milvus-io/pymilvus&style=plastic
