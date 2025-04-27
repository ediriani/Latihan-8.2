def hitung_frekuensi_kata(kalimat, kata_dicari):
    """
    Menghitung frekuensi kemunculan suatu kata dalam sebuah kalimat.

    Args:
        kalimat (str): Kalimat yang akan dianalisis.
        kata_dicari (str): Kata yang ingin dicari frekuensinya.

    Returns:
        int: Jumlah kemunculan kata dalam kalimat.
    """
    # Ubah kalimat dan kata yang dicari menjadi huruf kecil agar tidak case-sensitive
    kalimat = kalimat.lower()
    kata_dicari = kata_dicari.lower()

    # Pecah kalimat menjadi kata-kata
    kata_kata = kalimat.split()

    # Hitung frekuensi kemunculan kata
    frekuensi = kata_kata.count(kata_dicari)

    return frekuensi

# Contoh penggunaan
kalimat_input = "Saya mau makan. Makan itu wajib. Mau siang atau malam saya wajib makan"
kata_target = "makan"

jumlah_kemunculan = hitung_frekuensi_kata(kalimat_input, kata_target)
print(f"Kata '{kata_target}' ada {jumlah_kemunculan} buah")

kalimat_lain = input("Masukkan kalimat: ")
kata_lain = input("Masukkan kata yang ingin dicari frekuensinya: ")
jumlah_lain = hitung_frekuensi_kata(kalimat_lain, kata_lain)
print(f"Kata '{kata_lain}' ada {jumlah_lain} buah dalam kalimat tersebut.")
