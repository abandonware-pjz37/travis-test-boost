Builds done for 3 compilers:
* `linux.gcc` (language: cpp, compiler: gcc)
* `linux.clang` (language: cpp, compiler: clang)
* `mac.clang` (language: objective-c)

### Test mac
* `mac.clang` (**failed**: by default boost is not installed):
[![Build Status][link_mac_clang]][link_branches]

* `mac.clang.boost.install` (**passed**)
[![Build Status][link_mac_clang_boost_install]][link_branches]

* `mac.clang.boost-libcxx.install` (**failed**: brew install hangs):
[![Build Status][link_mac_clang_boost_libcxx_install]][link_branches]

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
[![Build Status][link_linux_gcc]][link_branches]
 * `linux.clang`
[![Build Status][link_linux_clang]][link_branches]

* Install boost fix it (**passed**):
 * `linux.gcc.boost.install`
[![Build Status][link_linux_gcc_boost_install]][link_branches]
 * `linux.clang.boost.install`
[![Build Status][link_linux_clang_boost_install]][link_branches]

* Try to detect boost 1.53 (**failed**: default version is lower):
 * `linux.gcc.boost-1.53`
[![Build Status][link_linux_gcc_boost_1_53]][link_branches]
 * `linux.clang.boost-1.53`
[![Build Status][link_linux_clang_boost_1_53]][link_branches]

* Try to install boost 1.53 explicitly (**failed**: no such package):
 * `linux.gcc.boost-1.53.explicit`
[![Build Status][link_linux_gcc_boost_1_53_explicit]][link_branches]
 * `linux.clang.boost-1.53.explicit`
[![Build Status][link_linux_clang_boost_1_53_explicit]][link_branches]

* Add external repository for boost-1.53 (**passed**):
 * `linux.gcc.boost-1.53.external`
[![Build Status][link_linux_gcc_boost_1_53_external]][link_branches]
 * `linux.clang.boost-1.53.external`
[![Build Status][link_linux_clang_boost_1_53_external]][link_branches]

[link_branches]: https://travis-ci.org/travis-ci-tester/travis-test-boost

[link_mac_clang]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=mac.clang
[link_mac_clang_boost_install]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=mac.clang.boost.install
[link_mac_clang_boost_libcxx_install]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=mac.clang.boost-libcxx.install
[link_linux_gcc]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.gcc
[link_linux_clang]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.clang
[link_linux_gcc_boost_install]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.gcc.boost.install
[link_linux_clang_boost_install]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.clang.boost.install
[link_linux_gcc_boost_1_53]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.gcc.boost-1.53
[link_linux_clang_boost_1_53]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.clang.boost-1.53
[link_linux_gcc_boost_1_53_explicit]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.gcc.boost-1.53.explicit
[link_linux_clang_boost_1_53_explicit]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.clang.boost-1.53.explicit
[link_linux_gcc_boost_1_53_external]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.gcc.boost-1.53.external
[link_linux_clang_boost_1_53_external]: https://travis-ci.org/travis-ci-tester/travis-test-boost.png?branch=linux.clang.boost-1.53.external
