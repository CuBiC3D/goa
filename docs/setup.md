# Development Setup

This document describes the steps required to setup a development environment for contributing to goa from scratch.

## 1. Install Go

The first step is to install the Go distribution. Please follow the steps described in the
[Go Getting Started guide](https://golang.org/doc/install)

## 2. Clone goa

    Note: This step requires `git`. Installing `git` is outside the scope of this document.

Once Go is installed and the [GOPATH](https://github.com/golang/go/wiki/SettingGOPATH) environment variable is set, clone goa:
```bash
cd $GOPATH/src
mkdir -p github.com/goadesign
cd github.com/goadesign
git clone https://github.com/goadesign/goa
```

## 3. Install goa dependencies

Bring in all the Go packages goa depends on:
```bash
cd goa
go get -v -u ./...
```

## 4. Build goa

Install the goa tool:
```bash
cd cmd/goa
go install .
```

## 5. Test the setup

Finally to make sure everything is properly setup run the tests:
```bash
cd $GOPATH/src/github.com/goadesign/goa
make
```