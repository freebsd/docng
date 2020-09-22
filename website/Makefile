#
# Generate the FreeBSD website
#
# Copyright (c) 2020 The FreeBSD Documentation Project
# Copyright (c) 2020 Sergio Carlavilla

# $FreeBSD$

# Targets intended for use on the command line
#
# all (default)	-	generate the releases.toml and compile all the website
# compile	-	generate the releases.toml and build all the website

MAINTAINER=carlavilla@FreeBSD.org

PYTHON_CMD =	/usr/local/bin/python3.7
HUGO_CMD =	/usr/local/bin/hugo

all: starting-message generate-releases run
compile: starting-message generate-releases build

starting-message:
	@echo ---------------------------------------------------------------
	@echo                   Building the website
	@echo ---------------------------------------------------------------

generate-releases:
	${PYTHON_CMD} ./tools/releases-toml.py -p ./share/releases.adoc

run:
	${HUGO_CMD} server -D

build:
	${HUGO_CMD} --minify


