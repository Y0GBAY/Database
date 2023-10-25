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


# Catatan Command Pertemuan 2

Belajar CRUD (Create Update Delete)

Untuk semua data 
```psql
SELECT * FROM user;
SELECT * FROM public.user;
```

Untuk Menambahkan data
```psql
INSERT INTO public.user (nama, saldo) VALUES ('Yoga Bayu', 0);
```

Untuk Update data
```psql
UPDATE public.user SET saldo=10000 WHERE id=1;
```

Untuk Menghapus Data
```psql
DELETE FROM public.user WHERE id=1;
```

Untuk merelasikan atau menghubungkan antar table
```psql
ALTER TABLE public.provider ADD CONSTRAINT fk_user FOREIGN KEY (user_id) REFERENCES public.user(id);
```

Untuk mengurutkan data berdasarkan abjad
```psql
SELECT * FROM mahasiswa order by nama_mahasiswa asc;
```

Untuk membuat relasi pada table
``` psql
 ALTER TABLE tabel1 ADD CONSTRAINT fk_tabel1 FOREIGN KEY (mahasiswa_id) REFERENCES tabel2(id);
```

Join table / melihat table bergabung
``` psql
 SELECT * FROM tabel1 AS dm INNER JOIN tabel2 AS dd ON dd.id=dm.mahasiswa_id;
 ```


