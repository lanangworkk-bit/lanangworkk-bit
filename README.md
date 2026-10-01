# Lanang Work

Mahasiswa yang sedang belajar membangun backend dari nol, layer demi
layer. Setiap semester saya bangun ulang aplikasi yang sama dengan
batasan yang lebih berat, dan setiap revisi saya simpan sebagai branch
supaya progresnya kelihatan.

## Yang sedang dipelajari

- **Backend**: Flask, SQLAlchemy, Alembic, JWT, Docker
- **Database**: pemodelan relasional, migrasi skema, pengoptimalan query
- **Kebiasaan**: test otomatis sebelum commit, CI sebagai pagar mutu

## Proyek

### [CampusFlow](https://github.com/lanangworkk-bit/CampusFlow)

Pengelola tugas kuliah pribadi. Backend Flask dengan SQLAlchemy dan
Alembic, satu basis kode untuk SQLite (default) dan PostgreSQL.

Yang membuatnya menarik: branch `semester-8` adalah versi
production-ready, sementara branch `main` masih versi semester 1 berbasis
localStorage. Perbedaannya menunjukkan apa yang saya pelajari selama
sisa semester.

- Autentikasi JWT dengan dua peran, dan setiap pengguna hanya melihat
  datanya sendiri
- Empat status yang saling lepas: `OVERDUE` dihitung ulang dari
  tenggat, bukan disimpan, jadi tidak pernah basi
- Agregasi analitik dijalankan database, bukan Python, setelah melihat
  `EXPLAIN` bahwa index sudah dipakai tapi ORM tetap jadi bottleneck
- 274 test: 254 biasa dan 20 yang menjalankan Chromium sungguhan
- Docker Compose dengan PostgreSQL dan Redis; enam job CI

**Stack:** Python, Flask, SQLAlchemy, Alembic, PostgreSQL, Redis,
Docker, Playwright

## Repo lain

- [focusguard-website](https://github.com/lanangworkk-bit/focusguard-website)
  - website dengan JavaScript
- [genre-finder](https://github.com/lanangworkk-bit/genre-finder)
  - aplikasi PHP untuk mencari genre
