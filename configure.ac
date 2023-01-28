AC_INIT

orig_CFLAGS="$CFLAGS"

AC_CONFIG_SRCDIR([ev_epoll.c])

dnl also update ev.h!
AM_INIT_AUTOMAKE(libev,4.22)
AC_CONFIG_HEADERS([config.h])
AM_MAINTAINER_MODE

AC_PROG_CC

dnl Supply default CFLAGS, if not specified
if test -z "$orig_CFLAGS"; then
  if test x$GCC = xyes; then
    CFLAGS="-g -O3"
  fi
fi

AC_SUBST(libdir, "/usr/local/lib/evlua")
AC_SUBST(includedir, "/usr/local/include/evlua")
AC_SUBST(mandir, "/usr/local/share/man/evlua")

AC_PROG_INSTALL
AC_PROG_LIBTOOL


m4_include([libev.m4])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
