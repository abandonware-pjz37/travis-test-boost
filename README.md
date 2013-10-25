Builds done for 3 compilers:
* `linux.gcc` (language: cpp, compiler: gcc)
* `linux.clang` (language: cpp, compiler: clang)
* `mac.clang` (language: objective-c, compiler: clang)

### Tests and branch names:
* Try to find boost and include `boost/config.hpp` (**failed**: by default boost is not installed):
 * `linux.gcc`
 * `linux.clang`
 * `mac.clang`

* Install boost fix it (**passed**):
 * `linux.gcc.boost.install`
 * `linux.clang.boost.install`
 * `mac.clang.boost.install`

* Try to detect boost 1.53 (**failed**: default version is lower):
 * `linux.gcc.boost-1.53`
 * `linux.clang.boost-1.53`
 * `mac.clang.boost-1.53`

* Try to install boost 1.53 explicitly (**failed**: no such package):
 * `linux.gcc.boost-1.53.explicit`
 * `linux.clang.boost-1.53.explicit`
 * `mac.clang.boost-1.53.explicit`

* Add external repository for boost-1.53 (**passed**):
 * `linux.gcc.boost-1.53.external`
 * `linux.clang.boost-1.53.external`
 * `mac.clang.boost-1.53.external`
