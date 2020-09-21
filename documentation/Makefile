#
# Generate the FreeBSD documentation
#
# Copyright (c) 2020 The FreeBSD Documentation Project
# Copyright (c) 2020 Sergio Carlavilla

# $FreeBSD$

# Targets intended for use on the command line
#
# all (default)	-	generate the Handbook TOC and compile all the documentation
# compile	-	generate the Handbook TOC and build all the documentation

MAINTAINER=carlavilla@FreeBSD.org

PYTHON_CMD =	/usr/local/bin/python3.7
HUGO_CMD =	/usr/local/bin/hugo

all: starting-message generate-handbook-toc run
compile: starting-message generate-handbook-toc build

starting-message:
	@echo ---------------------------------------------------------------
	@echo                   Building the documentation
	@echo ---------------------------------------------------------------

generate-handbook-toc:
	${PYTHON_CMD} ./tools/handbook-toc-creator.py -l en

run:
	${HUGO_CMD} server -D

build:
	${HUGO_CMD} --minify


