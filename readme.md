# instructions

This is for building files required for https://github.com/pyramation/node-pg-query-native which is a dependancy for https://github.com/pyramation/pg-query-parser

## 1

first download the `libpg_query` into the root of this project:

```sh
git clone git@github.com:lfittl/libpg_query.git
```
## 2

start the server

```sh
docker run -d \
  -it \
  --name build_pg_query \
  --mount type=bind,source="$(pwd)"/libpg_query,target=/pg_query \
  pyramation/libpg_query
```


## 3 build it and save the files

for example of what happens, check this

libpg_query/linux/libpg_query.a

https://github.com/pyramation/node-pg-query-native/commit/cff633ea55effb719c59b726bc1c6e838bd7c511

