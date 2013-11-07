help2man = @HELP2MAN@


info_TEXINFOS =	flex.texi
dist_man_MANS = flex.1
dist_doc_DATA = flex.pdf

EXTRA_DIST = $(info_TEXINFOS) $(PDFS) flex.dvi

CLEANFILES = \
	flex.hks \
	flex.ops

$(dist_man_MANS): $(top_srcdir)/main.c
	for i in $(dist_man_MANS) ; do \
	$(help2man) --name='$(PACKAGE_NAME)' \
	--section=`echo $$i | sed -e 's/.*\.\([^.]*\)$$/\1/'` \
	 ../flex$(EXEEXT) > $$i || rm -f $$i ; \
	done


clean-aminfo:
