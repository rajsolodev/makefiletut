include .env
export

.PHONY: build hello bye start setup install migrate run

NAME=Rajesh

hello:
	echo "Hello Makefile"

bye:
	echo "Bye Makefile"

start:
	echo "starting server..."

build:
	echo "production build...."

myname:
	echo "My Name is ${NAME}"

setup: install migrate run

install:
	echo "All Package installed"

migrate:
	echo "Database Migrated"

runserve:
	echo "Server start..."

showdb:
	echo "DBNAME: $(DB_NAME)"

ENV=prod

ifeq ($(ENV), dev)
run:
	echo "DEV mode ON"
else
run:
	echo "DEV Mode OFF"
endif

FILE=app/main.py

ifeq ($(wildcard $(FILE)),)
check:
	echo "File not found"
else
check:
	echo "file exists"
endif

USER=guest
ifeq ($(USER), admin)
who:
	echo "Admin User"
else
who:
	echo "Guest User"
endif

VERSION=2.0

ifneq ($(VERSION), 1.0)
info:
	echo "Not 1.0"
else
info:
	echo "1.0 Correct Version"
endif

TEXT= hello_world_from_make
replace:
	echo $(subst _, ,$(TEXT))

MYFILES = a.py b.py c.py
convert:
	echo $(patsubst %.py,%.txt,$(MYFILES))

PYFILES = $(wildcard *.py)
show:
	echo $(PYFILES)

STUDENTS = raj ram suman
loop:
	@$(foreach n, $(STUDENTS), echo STU: $(n))

MYENV ?= prod
ifeq ($(MYENV),dev)
myrun:
	echo "DEV MODE"
else
myrun:
	echo "PROD MODE"
endif