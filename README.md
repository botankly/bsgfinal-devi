# NeoShift - Lightweight Block Cipher Algorithm
NeoShift, Java ile geliştirilmiş, basitleştirilmiş bir blok şifreleme (Block Cipher) algoritmasıdır. Modern kriptografinin temel taşları olan Karıştırma (Confusion) ve Yayılma (Diffusion) prensiplerini kullanarak 8-byte'lık bloklar üzerinde simetrik şifreleme yapar.

 Özellikler
Simetrik Şifreleme: Şifreleme ve deşifreleme için aynı anahtar kullanılır.

Blok Tabanlı: Veriyi 8 byte (64-bit) uzunluğunda bloklar halinde işler.

Custom S-Box: Veriyi matematiksel olarak karıştırmak için özel bir İkame Tablosu (S-Box) kullanır.

Permütasyon: Verinin yapısını bozmak için bit/byte yer değiştirme işlemi uygular.

 Algoritma Nasıl Çalışır?
Algoritma üç temel aşamadan oluşur:

1. Anahtar Üretimi (Key Generation)
Verilen parola, modüler aritmetik kullanılarak tam 8 byte uzunluğunda bir şifreleme anahtarına dönüştürülür.

2. Şifreleme (Encryption)
XOR İşlemi: Düz metin, üretilen anahtar ile maskelenir.

İkame (Substitution): Her bir byte, önceden tanımlanmış S-Box tablosuna göre yeni bir değerle değiştirilir.

Permütasyon (Permutation): Bloğun ilk ve son byte'ı yer değiştirerek verinin yayılması sağlanır.

3. Deşifreleme (Decryption)
Şifreleme işleminin tam tersi sırayla uygulanmasıdır. Ters permütasyon, Ters S-Box (INV_SBOX) ve tekrar XOR işlemleri ile orijinal veriye ulaşılır.

 Kurulum ve Kullanım
Ön Koşullar
Java JDK 8 veya üzeri.

Çalıştırma
Projeyi klonladıktan sonra terminal üzerinden şu komutlarla çalıştırabilirsiniz:
javac NeoShiftProject.java
java NeoShiftProject
Örnek Kod Çıktısı
--- NeoShift Şifreleme Testi ---
Orijinal: GIZLI123
Şifreli Metin (Hex): 54586355526C467F
Deşifre Edilen: GIZLI123
