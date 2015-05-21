

##gemfile
group

##sql
```sql
select * from regions
select * from stores where region_id=1
select sales,store_id from orders order by sales desc
select sales,store_id from orders order by sales desc limit 5
select name from stores where id in (5,24,46,11,50)
select sales,store_id from orders where sales  between 100 and 200
select name from stores where name like 'E%';

select sales,stores.name from orders inner join stores on stores.id=orders.store_id order by sales desc limit 5

select count(*) from stores;
select sum(sales) from orders;

select count(*),regions.name from stores inner join regions on stores.region_id
=regions.id group by region_id;

select name from stores where id in (select store_id from orders order by sales desc limit 5)

select count(*) as store_count,regions.name from stores inner join regions on stores.region_id
=regions.id group by region_id having store_count>5;
```

```sql
show tables;
SHOW FULL COLUMNS FROM a03a3_group;
```

###add fk to rails 
```rb
    add_foreign_key "apply_jobs", "jobs",on_delete: :cascade
```

##rollbar

##keenio

##ga
