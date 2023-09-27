# Catatan command

create database
``` psql
    CREATE DATABASE yogbay_database;
```

pindah ke database
``` psql
    \c nama_database
```

Hapus Database
``` psql
    DROP DATABASE nama_database;
```

Membuat Table
``` psql
    CREATE TABLE public.user (
    id SERIAL PRIMARY KEY,
    nama VARCHAR(100),
    saldo INT );
```

Melihat Table 
``` psql
    \dt
    \d public.user
```
