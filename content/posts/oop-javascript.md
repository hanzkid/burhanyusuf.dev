---
title: OOP Javascript ( Bagian 1 )
date: 2020-12-20
published: true
tags: ['Javascript', 'OOP']
series: true
cover_image: https://dev-to-uploads.s3.amazonaws.com/i/khadboi9m4w04slcx77c.png
canonical_url: false
description: "OOP adalah salah satu konsep pemrograman selain Functional Programming."
---
OOP Pada JavaScript

Pada catatan kali ini, saya ingin berbagi apa yang saya pelajari tentang konsep OOP ( Object-oriented Programmin ) pada JavaScript. Beberapa kata kunci yang akan dipelajari yaitu Class, Object, Constructor, Method, Property.

<h3>Class</h3>
<p>
Class adalah sebuah <em>blueprint</em> pada konsep OOP. Secara umum, pengertian <em>blueprint</em> berdasarkan <em> Oxford Dictionary</em> adalah deskripsi yang mendetil mengenai suatu rencana. Dalam hal pemrograman, <em>class</em> adalah rancangan struktur awal dari objek yang akan dibuat. Misalnya kita ingin membuat sebuah objek yang memuat data dan fungsi dari mobil, maka sebelum kita membuat objek mobil tersebut, kita akan membuat sebuah class terlebih dahulu.
</p>
<pre>
<code class="language-javascript">

    class mobil{
        merk;
        harga;
        statusFuel;

        checkFuel(){
            return `this.statusFuel L`;
        }
    }

</code>
</pre>
Pada snippet diatas, class mobil memiliki data : merk, harga, dan statusFuel dan fungsi : checkFuel.

<h3>Property</h3>

Property adalah data yang ada pada sebuah class yang juga akan dimiliki oleh objek dari class tersebut. Property pada class mobil ada 3 yaitu : merk, harga, dan statusFuel.

<h3>Object</h3>
<p>
Object adalah satu data tunggal yang memiliki struktur dari sebuah class. Contoh pembuatan sebuah objek.
</p>
<pre>
<code class="language-javascript">

    let mobilPertamaSaya = new mobil();
    mobilPertamaSaya.merk = 'BMW';
    console.log(mobilPertamaSaya.merk); // BMW;

</code>
</pre>

Snippet diatas berisi :
<ul>
<li> Membuat objek bernama ` mobilPertamaSaya ` dari class mobil. </li> 
<li> Mengisi data merk dengan nilai ` BMW ` </li>
<li> Menampilkan data `merk` pada objek `mobilPertamaSaya`.</li>
</ul>
<h3>Constructor</h3>
<p>
Constructor adalah sebuah method yang akan langsung dijalankan ketika sebuah objek dibuat. Contoh constructor :
</p>
<pre>
<code class="language-javascript">

    class mobil{
        merk;
        harga;
        statusFuel = 100;

        constructor(merk,harga){
            this.merk = merk;
            this.harga = harga;
        }

        checkFuel(){
            return `this.statusFuel l`;
        }

    }

    let mobilPertamaSaya = new mobil('BMW',1000000);
    console.log(mobilPertamaSaya.merk);

</code>
</pre>

Snippet diatas berisi :
<ul>
<li> Fungsi constructor di class mobil akan menerima parameter merk dan harga ketika sebuah objek dibuat.
<ol>
<li> This pada fungsi constructor merujuk pada nilai sebuah objek. Dalam snippet diatas, this menunjukan objek mobilPertamaSaya.</li>
<li>This.merk = merk berfungsi memberi nilai merk pada objek mobilPertamaSaya dengan nilai merk yang dijadikan parameter saat inisialisasi objek dalam hal snippet ini ( <code>let mobilPertamaSaya = new mobil('BMW',1000000); </code>) adalah string BMW.</li>
</ol>
</li>
</ul>

<h3>Method</h3>
Method / fungsi / behaviour adalah segala sesuatu yang bisa dilakukan oleh sebuah objek. Pada class mobil kita akan membuat 2 fungsi baru, sehingga objek dari mobilPertamaSaya dapat melakukan 3 method;
<ul>
<li>checkFuel : untuk mengecek bahan bakar sekarang.</li>
<li>updateFuel : untuk memperbarui data bahan bakar setelah digunakan beberapa km. ( asumsi berkurang 1 l setiap 10 km )</li>
<li>fillFuel : untuk memperbarui data bahar bakar setelah diisi dengan parameter berapa jumlah pengisian ( dalam l ) </li>
</ul>
<pre>
<code class="language-javascript">
<pre class="language-text">
<code class="language-text">

    class mobil{
        merk;
        harga;
        statusFuel = 100;

        constructor(merk,harga){
            this.merk = merk;
            this.harga = harga;
        }

        checkFuel(){
            return this.statusFuel l;
        }

        updateFuel(jarak){
            this.statusFuel -= ( jarak / 10 );
            return this.checkFuel();
        }

        fillFuel(liter){
            this.statusFuel += liter;
            return this.checkFuel();
        }
    }

    let mobilPertamaSaya = new mobil('BMW',1000000);
    mobilPertamaSaya.updateFuel(10) // mobil melakukan perjalanan sejauh 10 km , dan akan mengembalikan nilai bahan bakar sekarang yaitu = 100 - ( 10 / 10 ) = 99
    mobilPertamaSaya.fillFuel(10) // mobil mengisi bahan bakar sebanyak 10 l, dan akan mengembalikan nilai bahan bakar sekarang yaitu = 100 + 10  = 109

</code>
</pre>
</code>
</pre>
