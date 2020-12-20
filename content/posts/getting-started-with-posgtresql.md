---
title: Getting Started With PostgreSQL
date: 2020-12-20
published: true
tags: ['SQL', 'PostgreSQL']
series: false
cover_image: https://miro.medium.com/max/800/1*PY24xlr4TpOkXW04HUoqrQ.jpeg
canonical_url: false
description: "PostgreSQL adalah salah satu RDBMS yang populer."
---
Memulai dengan PostgreSQL

Dalam SQL , terdapat 4 kelompok perintah yang sering digunakan, yaitu DML ( Data Manipulation Language ), DDL ( Data Definition Language ), TCL ( Transaction Control Language ), dan DCL ( Data Control Language ). Namun yang saya beri point utama adalah DML dan DDL.

<h2>Apa itu DDL?</h2>
DDL atau Data Definition Language adalah perintah yang berfungsi untuk menentukan / mengubah struktur dari sebuah database ataupun skema didalamnya. Beberapa perintah yaitu : CREATE, ALTER, DROP, RENAME.

<h3>Create</h3>
Create berfungsi untuk membuat sebuah database / skema / table baru pada RDBMS. Contoh penggunaan perintah CREATE :

CREATE DATABASE database_name : Untuk membuat sebuah database baru.
<img src="/images/postgresql-create-db.png" width="100%">

<h3>Apa itu DML?</h3>
DML atau Data Manipulation Language adalah perintah SQL yang digunakan untuk memanipulasi data. Beberapa perintah DML yang paling sering digunakan yaitu :
<ul> SELECT : 