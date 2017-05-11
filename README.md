## SQL*Plus Instant Client
SQL*Plus Instant Client is a standalone product with all the functionality of SQL*Plus command-line. It connects to existing remote Oracle databases, but does not include its own database. It is easy to install and uses significantly less disk space than the full Oracle Database Client installation required to use SQL*Plus command-line.


## Installing SQL*Plus Instant Client from the UNIX or Windows Zip Files

1- Download the zip files containing the SQL*Plus Instant Client package, and the OCI package from the OTN Instant Client page at 
   http://www.oracle.com/technology/tech/oci/instantclient/instantclient.html. 

### Linux Machines

A) Instant Client Package - Basic: All files required to run OCI, OCCI, and JDBC-OCI applications 
- instantclient-basic-linux.64-xxxxxx.zip

B) Instant Client Package - SDK: Additional header files and an example makefile for developing Oracle applications with Instant Client
- instantclient-sdk-linux.64-xxxxxx.zip

C) Instant Client Package - SQL*Plus: Additional libraries and executable for running SQL*Plus with Instant Client
- instantclient-sqlplus-linux.64-xxxxxx.zip

### MAC Machines

A) Instant Client Package - Basic: All files required to run OCI, OCCI, and JDBC-OCI applications 
- instantclient-basic-macos.x64-xx.x.x.x.x.zip

B) Instant Client Package - SDK: Additional header files and an example makefile for developing Oracle applications with Instant Client
- instantclient-sdk-macos.x64-xx.x.x.x.x.zip

C) Instant Client Package - SQL*Plus: Additional libraries and executable for running SQL*Plus with Instant Client
- instantclient-sqlplus-macos.x64-xx.x.x.x.x.zip

``` bash
unzip instantclient-basic-linux.64-xxxxxx.zip
unzip instantclient-sdk-linux.64-xxxxxx.zip
unzip instantclient-sqlplus-linux.64-xxxxxx.zip
```

For liunx machine only, in your current directory:

``` bash
cd instanceclient_12_1
ln -s libclntsh.so.12.1 libclntsh.so
ln -s libocci.so.12.1 libocci
```

For a quick run:

``` bash

export LD_LIBRARY_PATH=$(pwd)

./sqlplus hr/hr@localhost/pdboracle
```
To maintain library path, updated the ZSH and BASH to keep

``` bash
Add LD_LIBRARY_PATH to your .zsh or .bashrc.

vim ~/.zsh

export LD_LIBRARY_PATH=PATH_TO_YOUR_SQLPLUS_ROOT

```

### References
- [INSTALL SQLPLUS](https://www.youtube.com/watch?v=Sz69kdItkPw)
