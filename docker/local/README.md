# Monstache local builder

You can use the `build.sh` script in this folder to build monstache to your host machine using docker.

Run `build.sh` from this directory and the monstache binaries for all supported platforms (linux,win,mac)
will be built to a `docker-build` folder.

If your host is linux you may need to install `musl` to run the resulting binary. For example, on a debian system

```
sudo apt install musl
```

## common command

```shell
# 删除 index
curl -X DELETE "http://elastic:changeme@localhost:9200/dev-portal-user"
# 查询 index 中的数据
curl -X GET "http://elastic:changeme@localhost:9200/dev-portal-user/_search"
# 查看所有 index
curl -X GET "http://elastic:changeme@localhost:9200/_cat/indices"
# 连接本地测试数据库
mongo admin -u root-user -p password
mongo admin -u root-user-1 -p password
```

```js
// mongodb mock 数据
use test;

for (var i = 0; i < 100; i++) {
    db.test.insert({"name": i});
}
```
