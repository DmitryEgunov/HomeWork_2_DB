**SQL-запросы**

1. create table if not exists genre (id serial primary key, name varchar(20)not null);

2. create table if not exists artist (id serial primary key, name varchar(40) not null, genreid integer references genre(id));

3. create table if not exists album (id serial primary key, artistid integer references artist(id), name varchar(40) not null, releaseyear date);

4. create table if not exists track (id serial primary key, albumid integer references album(id), name varchar(60) not null, duration numeric(5,2));

**Результат**

!(http://)
