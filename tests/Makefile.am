include $(top_srcdir)/common.mk
MAXIMA = @POSIX_SHELL@ $(top_builddir)/maxima-local

TESTS =

if CLISP
TESTS += clisp-test.sh
clisp-test.sh: test.sh.in
	sed <"$<" >"$@"                                          \
	  -e 's#!LOCAL_MAXIMA!#$(MAXIMA)#'                       \
	  -e 's#!LISPNAME!#clisp#'                               \
	  -e 's#!OUTPUT_LOG!#$(top_builddir)/tests/clisp.log#'
	chmod a+x "$@"
endif

if CMUCL
TESTS += cmucl-test.sh
cmucl-test.sh: test.sh.in
	sed <"$<" >"$@"                                          \
	  -e 's#!LOCAL_MAXIMA!#$(MAXIMA)#'                       \
	  -e 's#!LISPNAME!#cmucl#'                               \
	  -e 's#!OUTPUT_LOG!#$(top_builddir)/tests/cmucl.log#'
	chmod a+x "$@"
endif

if SCL
TESTS += scl-test.sh
scl-test.sh: test.sh.in
	sed <"$<" >"$@"                                          \
	  -e 's#!LOCAL_MAXIMA!#$(MAXIMA)#'                       \
	  -e 's#!LISPNAME!#scl#'                                 \
	  -e 's#!OUTPUT_LOG!#$(top_builddir)/tests/scl.log#'
	chmod a+x "$@"
endif

if SBCL
TESTS += sbcl-test.sh
sbcl-test.sh: test.sh.in
	sed <"$<" >"$@"                                          \
	  -e 's#!LOCAL_MAXIMA!#$(MAXIMA)#'                       \
	  -e 's#!LISPNAME!#sbcl#'                                \
	  -e 's#!OUTPUT_LOG!#$(top_builddir)/tests/sbcl.log#'
	chmod a+x "$@"
endif

if GCL
TESTS += gcl-test.sh
gcl-test.sh: test.sh.in
	sed <"$<" >"$@"                                          \
	  -e 's#!LOCAL_MAXIMA!#$(MAXIMA)#'                       \
	  -e 's#!LISPNAME!#gcl#'                                 \
	  -e 's#!OUTPUT_LOG!#$(top_builddir)/tests/gcl.log#'
	chmod a+x "$@"
endif

if ACL
TESTS += acl-test.sh
acl-test.sh: test.sh.in
	sed <"$<" >"$@"                                          \
	  -e 's#!LOCAL_MAXIMA!#$(MAXIMA)#'                       \
	  -e 's#!LISPNAME!#acl#'                                 \
	  -e 's#!OUTPUT_LOG!#$(top_builddir)/tests/acl.log#'
	chmod a+x "$@"
endif

if OPENMCL
TESTS += openmcl-test.sh
openmcl-test.sh: test.sh.in
	sed <"$<" >"$@"                                          \
	  -e 's#!LOCAL_MAXIMA!#$(MAXIMA)#'                       \
	  -e 's#!LISPNAME!#openmcl#'                             \
	  -e 's#!OUTPUT_LOG!#$(top_builddir)/tests/openmcl.log#'
	chmod a+x "$@"
endif

if ECL
TESTS += ecl-test.sh
ecl-test.sh: test.sh.in
	sed <"$<" >"$@"                                          \
	  -e 's#!LOCAL_MAXIMA!#$(MAXIMA)#'                       \
	  -e 's#!LISPNAME!#ecl#'                                 \
	  -e 's#!OUTPUT_LOG!#$(top_builddir)/tests/ecl.log#'
	chmod a+x "$@"
endif

genericdir = $(insttestsdir)
genericdirDATA = $(wildcard $(addprefix $(srcdir)/, README.how-to mcond_display_elseif.out *.mac *.lisp wester_problems/*))

EXTRA_DIST = $(genericdirDATA) test.sh.in
