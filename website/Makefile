SHELL := /bin/bash
BUNDLE := bundle
JEKYLL := $(BUNDLE) exec jekyll

.PHONY: all install update clean build serve

all: install build

install: 
	$(BUNDLE) config --global silence_root_warning 1
	$(BUNDLE) config --global disable_platform_warnings true
	$(BUNDLE) config set path 'vendor/bundle'
	$(BUNDLE) install

update: 
	$(BUNDLE) update

clean: 
	$(JEKYLL) clean

build: 
	$(JEKYLL) build

serve: 
	$(JEKYLL) serve
