# UAS-PROJECT

## Link Video Pengerjaan
https://youtu.be/NDYHonxdI7Y?si=C1xGpIHYJkkw4YVx

## berikut kode program project UAS


```python
# Dictionary berisi menu makanan dan harganya
menu = {
    'Ayam_Penyet': 17000,
    'nasi_uduk': 10000,
    'batagor': 10000,
    'es_teh': 5000,
    'air_mineral': 4000,
    'jus_mangga': 13000
}

def tampilkan_menu():
    print("Menu Makanan/Minuman:")
    for item, harga in menu.items():
        print(f"{item.capitalize()}: Rp {harga}")

def hitung_total(pesanan):
    total = 0
    for pesanan_item in pesanan:
        if pesanan_item in menu:
            total += menu[pesanan_item]
    return total

def cetak_struk(pesanan, total_harga):
    print("\n--- Struk Pembelian ---")
    for item in pesanan:
        print(f"{item.capitalize()}: Rp {menu[item]}")
    print(f"Total Harga: Rp {total_harga}")
    print("--- Terima kasih telah berbelanja! ---")

def kasir_kantin():
    pesanan = []
    while True:
        tampilkan_menu()
        pilihan = input("Masukkan pesanan Anda (atau ketik 'selesai' untuk selesai berbelanja): ").lower()
        
        if pilihan == 'selesai':
            break
        elif pilihan in menu:
            pesanan.append(pilihan)
        else:
            print("Maaf, pesanan tidak valid. Silakan pilih dari menu yang tersedia.")
    
    total_harga = hitung_total(pesanan)
    cetak_struk(pesanan, total_harga)

# Jalankan program kasir kantin
kasir_kantin()
```

