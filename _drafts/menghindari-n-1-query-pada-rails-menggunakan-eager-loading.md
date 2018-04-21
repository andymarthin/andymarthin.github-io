---
layout: post
title: Menghindari N+1 Query pada rails menggunakan eager loading
author: Andy Marthin
date: 2018-04-22
categories:
- Ruby on Rails
---

Salah satu penyebab lambatnya app yang dibangun menggunakan rails adalah N +1 query.
Sebagai contoh ada sebuah Post dengan banyak tags, saat post di akses maka akan mengambil semua tags yang berhubungan dengan post tersebut. Kebanyakan ORM saat ini mengaktifkan Lazy Loading secara default, jadi ketika akan mengambil tag yang ada pada post ia akan melakukan query 1 per 1 sehingga akan membanjiri database. seharusnya query untuk mengambil tags cukup 1 query saja.

<!--more-->
