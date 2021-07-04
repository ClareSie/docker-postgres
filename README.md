# docker-postgres

* 2021/07/04
* 目的: 嘗試用 docker images 建立 PostgreSQL
    * [Running PostgreSql in a Container on Windows 10](https://dotnetninja.net/2020/02/running-postgresql-in-a-container-on-windows-10/)
    * [\[Docker\] 於 Windows 中運行 PostgreSQL Container 來提供本機 DB 開發環境](https://www.dotblogs.com.tw/wasichris/2020/11/13/104023)
* 問題: 
在 db_postgres 裡面的 volumes 設定需給定在本機端的存放路徑(我先在 E:/ 建立一個 db_data 資料夾)
```yaml=
    volumes: 
      - E:db_data:/var/lib/postgresql/data
```
若是寫成如下，則無法順利連進去 DB (目前還在研究原因)
```yaml=
    volumes: 
      - psql:/var/lib/postgresql/data
volumes:
  psql:
```


