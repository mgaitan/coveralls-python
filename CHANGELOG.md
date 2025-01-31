<a name="1.8.0"></a>
## 1.8.0 (2019-06-02)

#### Features

* **flag:**  allow disabling SSL verification ([2e3b5c61](2e3b5c61))

#### Bug Fixes

* **git:**  fix support for case where git binary is missing ([5bbceaae](5bbceaae))

<a name="1.7.0"></a>
## 1.7.0 (2019-03-20)

#### Features

* **api:**  support pull requests on buildkite (#197) ([2700e3e2](2700e3e2))

#### Bug Fixes

* **cli:**  ensure upload failures trigger cli failures ([16192b84](16192b84))

<a name="1.6.0"></a>
## 1.6.0 (2019-02-18)

#### Features

* **support:**  add support for SemaphoreCI (#193) ([4e09918a](4e09918a))

<a name="1.5.1"></a>
## 1.5.1 (2018-09-28)

#### Features
* **git:**  omit git info when git isn't installed (#187) ([764956ea](764956ea))
  * ... instead of erroring. The fixes the v1.4.0 release of "supporting
    non-git repos" when the git binary is not installed.
  * Note that commit info can still be set with env vars, even in non-git
    repositories -- see the docs for more info!

#### Compatibility
* **python:**  include python 3.7 in matrix tests ([023d474](023d474))
  * previous versions of `coveralls-python` should be compatible with Python 3.7, no
    code changes were required to make tests pass

#### Internal
* remove `pytest-runner` as a dependency (#185) ([4cbbfcd](4cbbfcd))

<a name="1.5.0"></a>
## 1.5.0 (2018-08-31)

#### Features
* **cli:**  allow execution as a module (#184) ([b261a853](b261a853), closes [#183](183))

#### Bug Fixes
* **paths:**  ensure windows paths are normalized to posix ([661e0f54](661e0f54), closes [#153](153))

<a name="1.4.0"></a>
## 1.4.0 (2018-08-24)

#### Performance
* **git:**  call fallback git commands in fallback cases only ([e42095b4](e42095b4))

#### Features
* **env:**  support git env vars (#182) ([a1918e89](a1918e89))
  * This change also adds support for non-git repos.
* **flags:**  add ability to add named job (#181) ([f7ba07bf](f7ba07bf))

#### Compatibility
* **python:**  drop support for Python 3.3 ([dcb06fc1](dcb06fc1))

<a name="1.3.0"></a>
## 1.3.0 (2018-03-02)

#### Features
* **ci:**  add Travis PR support (#162) ([baf683ee](baf683ee))
* **cli:**  allow `service_name` override from cli flag or env var (#167) ([e8a98904](e8a98904))
* **coveralls-enterprise:**  add support for coveralls enterprise (#166) ([7383f377](7383f377))
* **git:**  silently omit git data when git is unavailable (#176) ([f9db83cd](f9db83cd))
* **jenkins:**
  *  add logic to parse `CI_PULL_REQUEST` env variable (#171) ([34a037f5](34a037f5))
  *  add support for jenkins (#160) ([4e8cd9ec](4e8cd9ec))

<a name="1.2.0"></a>
### 1.2.0 (2017-08-15)

#### Features
* **support:**  add support for AppVeyor CI ([1a62ce27](1a62ce27))
* **support:**  add support for BuildKite CI ([a58d6f9e](a58d6f9e))
* **support:**  add support for branch coverage ([e2413e38](e2413e38))
* **support:**  add support for parallel builds in Coveralls CI ([7ba3a589](7ba3a589))

#### Bug Fixes
* fix coverage count in cases of partial branch coverage ([b9ab7037](b9ab7037))
* fix SNI validation errors in python2 ([c5541263](c5541263))
* warn when PyYAML is missing ([711e9e4c](711e9e4c))

<a name="1.1"></a>
### 1.1 (2015-10-04)

#### Features
*   support for Circle CI

<a name="1.0"></a>
### 1.0 (2015-09-17)

#### Features
*   official coverage 4.0 support

<a name="1.0b1"></a>
### 1.0 (2015-08-14)

#### Features
*  coverage 4 beta support
*  codeship experimetal support (`CI_BRANCH` env variable)
*  drop python 3.2 support (as coverage 4 does not support it)
*  repo token usage is deprecated (but still supported) in favor of env variable.
*  error reporting is improved, exist status codes added

<a name="1.0a2"></a>
### 1.0a2 (2015-02-19)

#### Features
*  fix latest alpha coverage.py support
*  remove erroneous warning message when writing output to a file

<a name="1.0a1"></a>
### 1.0a1 (2015-02-19)

#### Features
*  **Backwards Incompatible**: make pyyaml optional. If you're using .coveralls.yml, make sure to install `coveralls[yaml]`
*  coverage 4 alpha support
*  allow debug and output options to work without `repo_token`
*  fix merge command for python 3.X

<a name="0.5"></a>
### 0.5 (2014-12-10)

#### Features
*  add option --output=<file> for saving json to file for possible merging with coverages from other languages
*  add merge command for sending coverage stats from multiple languages

<a name="0.4.4"></a>
### 0.4.4 (2014-09-28)

#### Features
*  proper fix coverage.py dependency version

<a name="0.4.3"></a>
### 0.4.3 (2014-09-28)

#### Features
*  fix coverage.py dependency version

<a name="0.4.2"></a>
### 0.4.2 (2014-05-05)

#### Features
*  handle 503 errors from coveralls.io

<a name="0.4.1"></a>
### 0.4.1 (2014-01-15)

#### Features
*  fix gitlog output with utf8

<a name="0.4"></a>
### 0.4 (2013-12-27)

#### Features
*  added support for --rcfile=<file> option to cli
*  improved docs: nosetests and troubleshooting sections added
*  added debug in case of UnicodeDecodeError
*  removed sh dependency in favor of Windows compatibility

<a name="0.3"></a>
### 0.3 (2013-10-02)

#### Features
*  added initial support for Circle CI
*  fixed Unicode not defined error in python 3

<a name="0.2"></a>
### 0.2 (2013-05-26)

#### Features
*  Python 3.2 and PyPy support
*  graceful handling of coverage exceptions
*  fixed UnicodeDecodeError in json encoding
*  improved readme

<a name="0.1.1"></a>
### 0.1.1 (2013-02-13)

#### Features
*  introduced `COVERALLS_REPO_TOKEN` environment variable as a fallback for Travis
*  removed `repo_token` from verbose output for security reasons

<a name="0.1"></a>
### 0.1 (2013-02-12)

#### Features
*  initial release
