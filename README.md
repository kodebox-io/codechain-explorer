# CodeChain Explorer [![Gitter](https://badges.gitter.im/CodeChain-io/codechain-explorer.svg)](https://gitter.im/CodeChain-io/codechain-explorer?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

CodeChain explorer is simple, easy to use, open source visualization tool for viewing activity on the underlying blockchain network

## Table of Contents
* [instll](https://github.com/CodeChain-io/codechain-explorer#Instll)
* [running for development](https://github.com/CodeChain-io/codechain-explorer#Running-for-development)
* [build for production](https://github.com/CodeChain-io/codechain-explorer#Running-for-production)

## Instll
### Requirements
Following are the software dependencies required to install and run CodeChain-explorer
* Latest version of [CodeChain](https://github.com/CodeChain-io/codechain)
* Nodejs v10.4.1
* ElasticSearch v6.2.4
### Download
Download CodeChain-explorer code at github repository
```
# git clone git@github.com:kodebox-io/codechain-explorer.git
# cd codechain-explorer
```
### Install package
Use yarn package manager for install packages
```
# yarn install
```
## Running for development
### Before start
* Get ready CodeChain with CodeChain RPC server
* Get ready ElasticSearch database for indexing block data
### Running order
1. Worker
- Data synchronizing tool between CodeChain and ElasticSearch
2. Server
- Restful api server for getting data from db
3. Client
- Client developed by react framework
### Worker
Run CodeChain-worker for indexing data to elasticsearch
* You can change ElasticSearch and CodeChain host url in "/worker/config/default.json"
```
# yarn run start-worker
```
### Server
Run CodeChain-explorer server
* You can change ElasticSearch and CodeChain host url in "/server/config/default.json"
```
# yarn run start-server
```
### Client
Run CodeChain-explorer client in development mode
```
# yarn run start
```
## Running for production
### Build
Build CodeChain-explorer with following script. You can get optimized, uglified build code. It will locate at "/build" directory
```
# yarn run build
```
