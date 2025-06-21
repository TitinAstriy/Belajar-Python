# Belajar-Pytho
while True:
    print("=== KALKULATOR SEDERHANA ===")
    print("Operasi yang tersedia: + - * / % ** //")

    try:
        angka1 = float(input("Masukkan angka pertama: "))
        operasi = input("Masukkan operasi (+, -, *, /, %, **, //): ")
        angka2 = float(input("Masukkan angka kedua: "))
       
        
        if operasi == "+":
            hasil = angka1 + angka2 
        elif operasi == "-":
            hasil = angka1 - angka2
        elif operasi == "*":
            hasil = angka1 * angka2
        elif operasi == "/":
            if angka2 != 0:
                hasil = angka1 / angka2
            else:
                print("Tidak dapat melakukan pembagian dengan nol.")
                hasil = None
                
        elif operasi == "%":
            hasil = angka1 % angka2
        elif operasi == "**":
            hasil = angka1 ** angka2
        
        elif operasi == "//":
            if angka2 != 0:
                hasil = angka1 // angka2
        else:
            print("Operasi tidak valid.")
            hasil = None
        
        if hasil is not None:
            if hasil.is_integer():
                print("Hasil operasi:", int(hasil))
            else:
                print("Hasil operasi:", hasil)

    except ValueError:
        print("Masukkan angka yang valid!")
        hasil = None

    # Tanyakan apakah pengguna ingin mengulang
    ulang = input("\nApakah Anda ingin menghitung lagi? (ya/tidak): ").lower()
    if ulang != "ya":
        print("Terima kasih telah menggunakan kalkulator!")
        break
