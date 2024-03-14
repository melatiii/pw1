print('----Hitung denda peminjaman buku perpustakaan----')


while True :
    Lama_peminjaman = int(input("Berapa lama meminjam buku ? : "))
    Denda_harian = 2000
    Denda_mingguan = 5000
    Denda_total = 0

    for i in range (1,Lama_peminjaman+1)  :
        if i > 7 :
            Denda_total += Denda_harian
            if i % 7 == 0 :
                Denda_total += Denda_mingguan
    if Lama_peminjaman > 7 :
        print(f"\nKamu telah meminjam buku lebih dari 1 Minggu\nKamu terlambat mengembalikan buku selama {Lama_peminjaman-7} hari dan kamu dikenai denda sebesar Rp.{Denda_total}  ")
        
    else :
        print(f"\nKamu meminjam buku selama {Lama_peminjaman} hari. Jadi kamu tidak dikenai denda \n Terima Kasih")

    ulangi = input("Ulangi menghitung (y/t) ? : ").lower()
    if ulangi == 't':
            print("Perhitungan denda pengembalian buku perpustakaan selesai. Terimakasih telah menggunakan layanan perpustakaan. Kembali lagi ya... yuk baca buku di perpus! ")
            break
