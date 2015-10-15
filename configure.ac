AC_INIT([text-classifier],[2.0])
AM_INIT_AUTOMAKE([foreign nostdinc subdir-objects])

AC_CONFIG_MACRO_DIR([m4])

m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

AC_CANONICAL_HOST

AC_GNU_SOURCE

# For libdivsufsort
AC_DEFINE(PROJECT_VERSION_FULL, [PACKAGE_VERSION], [Define to the version of this package.])

AM_PROG_AR
AM_PROG_CC_C_O
AM_PROG_LEX
AC_PROG_CXX
AC_PROG_INSTALL
AC_PROG_MAKE_SET

LT_INIT

AC_LANG_PUSH([C++])
AX_OPENMP()
AX_CXX_COMPILE_STDCXX_14([ext])
AC_LANG_POP([C++])

AC_LANG_PUSH([C])
AX_OPENMP()
AC_LANG_POP([C])

CFLAGS="$CFLAGS -fuse-ld=gold $OPENMP_CFLAGS"
CXXFLAGS="$CXXFLAGS -fuse-ld=gold $OPENMP_CXXFLAGS"

AC_CONFIG_HEADERS([config.h])
AC_CONFIG_FILES([Makefile])
AC_OUTPUT