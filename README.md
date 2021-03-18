# sysbench-tpcc

TPCC-like workload for sysbench 1.0.x.
**Make sure you are using sysbench 1.0.14 or better!**

# MySQL 

## prepare data and tables

`
./tpcc.lua --mysql-host=$mysql_address --mysql-user=root --mysql-db=sbt --time=300 --threads=64 --report-interval=1 --tables=10 --scale=100 --db-driver=mysql prepare
`


## Run benchmark

`
./tpcc.lua --mysql-host=$mysql_address --mysql-user=root --mysql-db=sbt --time=300 --threads=64 --report-interval=1 --tables=10 --scale=100 --db-driver=mysql run
`

## Cleanup 

`
./tpcc.lua --mysql-host=$mysql_address --mysql-user=root --mysql-db=sbt --time=300 --threads=64 --report-interval=1 --tables=10 --scale=100 --db-driver=mysql cleanup
`

# TiDB

## prepare data and tables

`
./tpcc.lua --mysql-host=$tidb_address --mysql-port=4000 --mysql-user=root --mysql-db=sbt --time=300 --threads=64 --report-interval=1 --tables=10 --scale=100 --db-driver=mysql prepare
`

## Run benchmark

`
./tpcc.lua --mysql-host=$tidb_address --mysql-port=4000 --mysql-user=root --mysql-db=sbt --time=300 --threads=64 --report-interval=1 --tables=10 --scale=100 --db-driver=mysql run
`

## Cleanup 

`
./tpcc.lua --mysql-host=$tidb_address --mysql-port=4000 --mysql-user=root --mysql-db=sbt --time=300 --threads=64 --report-interval=1 --tables=10 --scale=100 --db-driver=mysql cleanup
`