SUBDIRS = hooks

retracelib_PYTHON = \
    __init__.py \
    argparser.py \
    retrace.py \
    retrace_worker.py \
    stats.py \
    plugins.py \
    util.py

nodist_retracelib_PYTHON = \
    config.py

retracelibdir = $(pythondir)/retrace

EXTRA_DIST = config.py.in

config.py: config.py.in
	sed -e "s|@DF_BIN@|$(DF)|g" \
	    -e "s|@GZIP_BIN@|$(GZIP)|g" \
	    -e "s|@TAR_BIN@|$(TAR)|g" \
	    -e "s|@XZ_BIN@|$(XZ)|g" \
	    -e "s|@LSOF_BIN@|$(LSOF)|g" \
	    $< > $@
