# Associate dan Dissociate
*Associate* berfungsi untuk mengupdate data dan *Dissociate* berfungsi untuk menghapus data, Mereka berfungsi di relation **One to many** atau bisa dibilang untuk yang **belongsTo**

# Attach dan Detach
*Attach* berfungsi untuk menambahkan atau membuat baru data secara otomatis tanpa harus menggunakan metode create seperti biasa dan *Detach* berfungsi untuk menghapus data secara otomatis tanpa harus menggunakan metode delete seperti biasa, Mereka berfungsi di relation **Many to many(Banyak ke banyak)**

# Eager Loading
Berfungsi untuk melakukan query tambahan,melakukan nested atau pencabangan secara sekaligus dengan cara menambahkan method **with('')** pada controller anda, jika ingin menambahkan table yang ingin di *Eager Loading* maka tinggal tambahkan koma(,) dan buat menjadi array lagi.

# Has Many Through
Berfungsi untuk mengakses atau relation suatu table yang kita tidak berhubungan secara langsung tapi menggunakan perantara dengan cara menambahkan relation pada model yang ingin direlasikan.<br>

Contoh : **return $this->hasManyThrough('(parameter yang ingin diakses)', '(melalui model apa yang ingin berhubungan)');**

# Insert Relation Method
Berfungsi untuk menambahkan data secara otomatis tanpa harus memasukkan kolom tambahan dan bisa juga mengoper parameter kedua jika kita melakukan relation *Many to many*.<br>

Contoh : **$user->forums()->save($forum);** atau **$user->forums()->save($form, ['kolom' => $nilai]);**

# 