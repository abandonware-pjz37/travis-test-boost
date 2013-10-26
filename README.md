Builds done for 3 compilers:
* `linux.gcc` (language: cpp, compiler: gcc)
* `linux.clang` (language: cpp, compiler: clang)
* `mac.clang` (language: objective-c)

### Test mac
* `mac.clang` (**failed**: by default boost is not installed):
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=mac.clang)](https://travis-ci.org/travis-ci-tester/travis-test-boost)

* `mac.clang.boost.install` (**passed**)
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=mac.clang.boost.install)](https://travis-ci.org/travis-ci-tester/travis-test-boost)

* `mac.clang.boost-libcxx.install` (**failed**: brew install hangs):
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=mac.clang.boost-libcxx.install)](https://travis-ci.org/travis-ci-tester/travis-test-boost)

```
> brew install boost --with-c++11
...
No output has been received in the last 10 minutes, this potentially indicates a stalled build or something wrong with the build itself.
The build has been terminated
```
*Workaround*: link boost libraries dynamically


### Tests linux
* Try to find boost and include `boost/config.hpp` (**failed**: by default boost is not installed):
 * `linux.gcc`
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.gcc)](https://travis-ci.org/travis-ci-tester/travis-test-boost)
 * `linux.clang`
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.clang)](https://travis-ci.org/travis-ci-tester/travis-test-boost)

* Install boost fix it (**passed**):
 * `linux.gcc.boost.install`
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.gcc.boost.install)](https://travis-ci.org/travis-ci-tester/travis-test-boost)
 * `linux.clang.boost.install`
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.clang.boost.install)](https://travis-ci.org/travis-ci-tester/travis-test-boost)

* Try to detect boost 1.53 (**failed**: default version is lower):
 * `linux.gcc.boost-1.53`
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.gcc.boost-1.53)](https://travis-ci.org/travis-ci-tester/travis-test-boost)
 * `linux.clang.boost-1.53`
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.clang.boost-1.53)](https://travis-ci.org/travis-ci-tester/travis-test-boost)

* Try to install boost 1.53 explicitly (**failed**: no such package):
 * `linux.gcc.boost-1.53.explicit`
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.gcc.boost-1.53.explicit)](https://travis-ci.org/travis-ci-tester/travis-test-boost)
 * `linux.clang.boost-1.53.explicit`
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.clang.boost-1.53.explicit)](https://travis-ci.org/travis-ci-tester/travis-test-boost)

* Add external repository for boost-1.53 (**passed**):
 * `linux.gcc.boost-1.53.external`
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.gcc.boost-1.53.external)](https://travis-ci.org/travis-ci-tester/travis-test-boost)
 * `linux.clang.boost-1.53.external`
[![Build Status](https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.clang.boost-1.53.external)](https://travis-ci.org/travis-ci-tester/travis-test-boost)
