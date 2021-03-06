#
# %CopyrightBegin%
# 
# Copyright Ericsson AB 2009. All Rights Reserved.
# 
# The contents of this file are subject to the Erlang Public License,
# Version 1.1, (the "License"); you may not use this file except in
# compliance with the License. You should have received a copy of the
# Erlang Public License along with this software. If not, it can be
# retrieved online at http://www.erlang.org/.
# 
# Software distributed under the License is distributed on an "AS IS"
# basis, WITHOUT WARRANTY OF ANY KIND, either express or implied. See
# the License for the specific language governing rights and limitations
# under the License.
# 
# %CopyrightEnd%
#
#
include $(ERL_TOP)/make/target.mk
include $(ERL_TOP)/make/$(TARGET)/otp.mk

# ----------------------------------------------------
# Application version
# ----------------------------------------------------
include ../../vsn.mk
VSN=$(ERL_DOCGEN_VSN)

# ----------------------------------------------------
# Release directory specification
# ----------------------------------------------------
RELSYSDIR = $(RELEASE_PATH)/lib/erl_docgen-$(VSN)


# ----------------------------------------------------
# Target Specs
# ----------------------------------------------------


DTD_FILES = \
	application.dtd \
	chapter.dtd \
	common.header.dtd \
	comref.dtd \
	fileref.dtd	 \
	xhtml1-frameset.dtd \
	appref.dtd \
	cites.dtd \
	common.image.dtd \
	cref.dtd \
	part.dtd \
	xhtml1-strict.dtd \
	book.dtd \
	common.dtd \
	common.refs.dtd \
	erlref.dtd \
	report.dtd \
	xhtml1-transitional.dtd \
	bookinsidecover.dtd \
	common.entities.dtd \
	common.table.dtd \
	fascicules.dtd \
	terms.dtd



# ----------------------------------------------------
# FLAGS
# ----------------------------------------------------


# ----------------------------------------------------
# Targets
# ----------------------------------------------------
debug opt: 

docs:

clean:
	$(RM) $(TARGET_FILES)


# ----------------------------------------------------
# Release Target
# ---------------------------------------------------- 
include $(ERL_TOP)/make/otp_release_targets.mk


release_spec: opt
	$(INSTALL_DIR) $(RELSYSDIR)/priv/docbuilder_dtd
	$(INSTALL_DATA) $(DTD_FILES) $(RELSYSDIR)/priv/docbuilder_dtd


release_docs_spec:


release_tests_spec:


