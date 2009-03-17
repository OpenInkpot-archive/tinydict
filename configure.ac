AC_INIT(libtinydict, 0.1, vadim.lopatin@coolreader.org)

AM_INIT_AUTOMAKE(libtinydict, 0.1.0, vadim.lopatin@coolreader.org)

AC_PROG_CXX
AM_PROG_LIBTOOL

AC_ARG_WITH(jinke,AC_HELP_STRING([--with-jinke],[path to jinke SDK]),
    [
        ac_cv_use_jinke=$withval
        with_jinke=true
        case ${host_cpu} in
            i?86) cpu_libdir=i386 ;;
            *) cpu_libdir="${host_cpu}";;
        esac
        JINKEPATH="$withval"
        CPPFLAGS="${CPPFLAGS} -I${JINKEPATH}/include"
        LDFLAGS="${LDFLAGS} -L${JINKEPATH}/lib/${cpu_libdir}"
        export CPPFLAGS
        export LDFLAGS
        export JINKEPATH
        with_jinke=true
    ],[
        with_jinke=false
        ac_cv_use_jinke=none
	])
	
AM_CONDITIONAL(WITH_JINKE,$with_jinke)
	

AC_OUTPUT(Makefile libtinydict.pc)
