# Spring Batch ☕🚀

- Java >= 8
- Maven
- IntelliJ
- MySQL

<hr>

### Docker - MySQL

```
docker pull mysql:8.0.12
docker run -d -p 3306:3306 --name mysqldb -e MYSQL_ROOT_PASSWORD=secret mysql:8.0.12 --character-set-server=utf8mb4 --collation-server=utf8mb4_unicode_ci

docker exec -it mysqldb mysql -uroot -p

docker container ls -a
container rm -f XXX
```
<hr>

### SQL
```
CREATE SCHEMA `batch_db` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_spanish_ci;

use batch_db;

SELECT
count(*) records,
min(created_date) start,
max(created_date) end,
timediff(max(created_date), min(created_date)) elapsed_time
FROM customers_info
;

select *  from customers_info;

delete from customers_info where 1=1;
```

<hr>

### API - Start Job
```
//POST
http://localhost:9191/jobs/importCustomers
```

Thanks to &copy; @basahota