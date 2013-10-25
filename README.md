Builds done for 3 compilers: gcc (linux), clang (linux), clang (mac os x).
Below names of branches.

* try to find boost and include boost/config.hpp (failed: by default boost is not installed):
 * master
 * clang
 * mac

* install boost fix it (passed):
 * boost.install
 * clang.boost.install
 * mac.install

* try to detect boost 1.53 (failed: default version is lower):
 * boost-1.53
 * clang.boost-1.53
 * mac.boost-1.53

* try to install boost 1.53 explicitly (failed: no such package):
 * boost-1.53.explicit
 * clang.boost-1.53.explicit
 * mac.boost-1.53.explicit

* add external repository for boost-1.53 (passed):
 * boost-1.53.external
 * clang.boost-1.53.external
 * mac.boost-1.53.external
