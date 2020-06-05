## driver-IPFS (uplink v1.0.5)

[![Go Report Card](https://goreportcard.com/badge/github.com/storj-thirdparty/driver-IPFS)](https://goreportcard.com/report/github.com/storj-thirdparty/driver-IPFS)

## Overview

The IPFS Driver connects to an IPFS server, takes a backup of the specified files and uploads the backup data on Storj network.

```bash
Usage:
  driver-IPFS [command] <flags>

Available Commands:
  help        Help about any command
  store       Command to upload data to a Storj V3 network.
  download    Command to download data from a Storj V3 network.
  version     Prints the version of the tool

```

`store` - Connect to the specified IPFS (default: `ipfs_property.json`). Back-up of the IPFS is generated using tooling provided by IPFS and then uploaded to the Storj network.  Connect to a Storj v3 network using the access specified in the Storj configuration file (default: `storj_config.json`).

`download` - Connect to the specified IPFS (default: `ipfs_property.json`). Connect to a Storj v3 network using the access specified in the Storj configuration file (default: `storj_config.json`). Download the data using file hash and download location specified in the Storj download configuration file (default: `storj_download.json`).

Sample configuration files are provided in the `./config` folder.

##### Note: This driver can only be used for uploading and downloading files, directories are not yet supported.

## Requirements and Install

To build from scratch, [install the latest Go](https://golang.org/doc/install#install).

> Note: Ensure go modules are enabled (GO111MODULE=on)



#### Option #1: clone this repo (most common)

To clone the repo

```
git clone https://github.com/storj-thirdparty/driver-IPFS.git
```

Then, build the project using the following:

```
cd driver-IPFS
go build
```

#### Option #2:  ``go get`` into your gopath

 To download the project inside your GOPATH use the following command:

```
go get github.com/storj-thirdparty/driver-IPFS
```

## Connect to IPFS Server

Make sure you are connected to IPFS server. If not, run the ipfs daemon in another `terminal` to join your node to the public network:

```
$ ipfs daemon
```


## Run (short version)

Once you have built the project run the following commands as per your requirement:

##### Get help

```
$ ./driver-IPFS --help
```

##### Check version

```
$ ./driver-IPFS --version
```

##### Upload data from local storage using ipfs and upload to Storj

```
$ ./driver-IPFS store
```

##### Download backup from Storj using earlier created ipfs file hash

```
$ ./driver-IPFS download
```

## Documentation

For more information on runtime flags, configuration, testing, and diagrams, check out the [Detail](//github.com/storj-thirdparty/driver-IPFS/wiki/Home) or jump to:

* [Config Files](//github.com/storj-thirdparty/driver-IPFS/wiki/#config-files)
* [Run (long version)](//github.com/storj-thirdparty/driver-IPFS/wiki/#run)
* [Testing](//github.com/storj-thirdparty/driver-IPFS/wiki/#testing)
* [Data-Flow Diagram (Upload)](//github.com/storj-thirdparty/driver-IPFS/wiki/#data-flow-diagram-upload)
* [Data-Flow Diagram (Download)](//github.com/storj-thirdparty/driver-IPFS/wiki/#data-flow-diagram-download)
* [Work-Flow Diagram (Upload)](//github.com/storj-thirdparty/driver-IPFS/wiki/#work-flow-diagram-upload)
* [Work-Flow Diagram (Download)](//github.com/storj-thirdparty/driver-IPFS/wiki/#work-flow-diagram-download)
