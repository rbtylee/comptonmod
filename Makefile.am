MAINTAINERCLEANFILES = Makefile.in aclocal.m4 config.guess config.h.in \
		       config.sub configure depcomp install-sh ltmain.sh \
		       missing module.desktop config.rpath mkinstalldirs

SUBDIRS = src \
data

EDJE_FLAGS = -v \
	     -id $(top_srcdir)/data/images

filesdir = $(datadir)
files_DATA = module.desktop e-module-comptonmod.edj

EXTRA_DIST = module.desktop.in \
	     e_modules-comptonmod.spec.in \
	     e-module-comptonmod.edc \
	     data/images/module_icon.png

%.edj:  %.edc
	$(EDJE_CC) $(EDJE_FLAGS) $< $@

clean-local:
	 rm -rf e-module-comptonmod.edj module.desktop e_modules-comptonmod.spec *~

uninstall:
	rm -rf $(DESTDIR)$(datadir)
