# For Loops

```
for i in range(1,10):
    print(i)

print("loop bitti.")

"""
1
2
3
4
5
6
7
8
9
loop bitti.
"""
```

#### Tek sayıları yazdıran for döngüsü

```
for i in range(1,10,2):
    print(i)
    
print("end of loop.")
```

#### 10'dan 1'e geriye doğru 3'er azaltan for döngüsü
```
for i in range(10, 0, -3):
    print(i)

print("end of loop.")
```

#### word String ifadesinin her karakterini yazdıran for döngüsü
```
word = "Python"

for i in word:
    print(i)
```

### Örnek - 1
#### User'dan adını girmesini isteyelim ve adını üç kere ekrana bastıralım.

```
name = input("Adını gir.")
for i in range(0,3):
    print("Adım ", i)
    print(name)
```

### Örnek - 2 
#### Userdan bir sayı ve bir cümle iste, verdiği sayı kadar karakteri bastır. 

```
num = int(input("Sayı girin."))
name = input("Bir cümle girin.")

for i in range(0,num):
    print(name[i])
```

### Örnek - 3
#### Userdan bir sayı isteyip, o sayının 1-12 aralığında tüm sayılar ile teker teker çarpımlarını bastıralım.

```
num = int(input("Sayı:"))

for i in range(1,13):
    answer = i * num
    print(i, "*" , num, "=", answer)
```

#### Girilen değere göre name değişkenini bastıran ya da too high uyarısı veren kod 
```
name = input("İsim:")
num = int(input("Kaç defa ekrana bastırılsın?"))

if num <= 5:
    for i in range(0,num):
        print(name)
else:
    print("too high.")
```

#### Parti davetiye listesi. 
#### User kaç kişiyi davet etmek istediğini girer, ardından o kadar kez isim program tarafından talep edilir. 

```
num = int(input("Kaç kişiyi partiye davet etmek istiyorsun. "))
if num<=10:
    for i in range(0,num):
        name = input("Kişinin adı: ")
        print(name, " is invited.")
else:
    print("10dan fazla kişi çağıramazsın.")
```

# While Loops

```
cevap = "evet"

while cevap == "evet":
    print("hello")
    cevap = input("loopu tekrarlamak ister misin? ")

print("while loop bitti.")

"""
hello
loopu tekrarlamak ister misin? evet
hello
loopu tekrarlamak ister misin? evet
hello
loopu tekrarlamak ister misin? hayır
while loop bitti.
"""
```

### Örnek - 1 
#### belli bir sayıya kadar olan tüm sayıların toplamını her adımda görerek bulma.

```
num = int(input("Sayı: "))

toplam = 0
index = 1

while index <= num:
    toplam = toplam + index
    print("Adım ",index, ", Toplam: ",toplam)
    index = index + 1
```

### Örnek - 2
#### Userdan 10 ile 20 arasında bir sayı talep ediyorum, doğru sayı girilene kadar loop devam etsin. 

```
num = int(input("10 ile 20 arasında bir sayı giriniz. "))

while num<10 or num>20:
    if num<10:
        print("10'dan büyük olmalı.")
    elif num>20:
        print("20'den küçük olmalı.")
    num = int(input("Tekrar sayı giriniz: "))

print("Girilen sayı: ", num, " teşekkürler. ")
```

### Örnek -3 
#### Partiye davet etmek istediklerimizi while loop içerisinde ekleme.

```
cevap = "y"
kisi_sayisi = 0

while cevap == "y":
    name = input("Partiye kimi davet etmek istiyorsun? ")
    print(name, "partiye davet edildi.")
    kisi_sayisi += 1
    cevap = input("Baska birisini davet etmek istiyor musun? (y/n)")

print("Partine ", kisi_sayisi," kişi davet ettin. ")
```

### Örnek - 4 

#### Sayı tahmin oyunu

```
"""
Bir sayı belirle, kullanıcıdan sayıyı tahmin etmesini iste. 
Tahmin etmesi için ona 3 hak tanı. Hakları bitene kadar tahminlerini al. 
Hakları bitmeden sayıyı tahmin edebilirse tebrik et, edemezse tekrar dene yazdır.

"""

magic_number = 50
tahmin_sayisi = 2
tahmin = int(input("Tahmin: "))

while tahmin != magic_number and tahmin_sayisi != 0:
    if tahmin < magic_number:
        print("Tuttuğum sayı daha büyük.")
    else:
        print("Tuttuğum sayı daha küçük.")
    tahmin_sayisi -=1 
    tahmin = int(input("Yeniden tahmin et: "))
    
"""
if tahmin_sayisi == 0 and magic_number != tahmin:
    print("Hakların bitti. Tuttuğum sayı: ", magic_number)
elif magic_number == tahmin:
    print("Tebrikler. ", 3 - tahmin_sayisi, " tahminde bulabildin.")
"""

if magic_number == tahmin:
    print("Tebrikler")
else:
    if tahmin_sayisi== 0:
        print("Hakkın bitti.")    
```

# Random Kütüphanesi

```
import random

num = random.random()
num
```

### Örnek -1
#### belli bir aralıkta random tam sayı üreten program

```
num = random.randint(0,9)
num
```

### Örnek - 2 
#### bir aralıkta, belirlenen sayı adımlarından bir random sayı seçen program. 

```
num = random.randrange(0,100,5)
num
```

### Örnek - 3
#### bir grup renkten birisini random olarak seçen program.

```
renk_kumesi = ["kırmızı", "siyah", "mavi"]

sayi_kumesi = [1,2,3,7,8,11]

renk = random.choice(renk_kumesi)
print("Torbadan çıkan renk: ", renk)

sayi = random.choice(sayi_kumesi)
print("Torbadan çıkan sayi: ",sayi )
```

### Örnek -4
#### Yazi - tura tahmin oyunu 

```
paranin_yuzu = ["yazi", "tura"]

para = random.choice(paranin_yuzu)

tahmin = input("Yazı mı tura mı?")

if tahmin == para:
    print("Bildin!!!!")
else:
    print("Bilemedin, ", para ," idi.")
```

### Örnek - 5
#### Sayi tahmin oyunu
#### 1 ile 5 arasında rastgele bir sayı seçilsin, 2 hakta bilinmeye çalışılsın. 

```
sayi = random.randint(1,5)

if sayi % 2 == 0:
    print("ipucu: sayı 2'nin katı.")

tahmin = int(input("1 ile 5 arasında bir sayı tuttum, tahmin et. "))

if tahmin == sayi:
    print("Tebrikler!!!!")

elif tahmin < sayi:
    print("Tuttuğum sayı daha büyük.")
    tahmin = int(input("Tekrar tahmin et."))
    if tahmin == sayi:
        print("Doğru.")
    else:
        print("Kaybettin.")

elif tahmin > sayi: 
    print("Tuttuğum sayı daha küçük.")
    tahmin = int(input("Tekrar tahmin et."))
    if tahmin == sayi:
        print("Doğru.")
    else:
        print("Kaybettin.")
```

### Örnek - 5
```
hayvanlar = ["kedi", "köpek", "kuş", "balık", "karınca"]

hayvan = random.choice(hayvanlar)

cevap = False

print("Kedi, köpek, kuş, balık ve karınca.")
while cevap == False:
    tahmin = input("Birisini gördüm, sence ne? ")
    tahmin = tahmin.lower()
    
    if tahmin == hayvan:
        print("Bildin, bir ", hayvan, " gördüm. ")
        cevap = True
    
    else:
        print("Bilemedin, başka bir hayvan.")
```


# Tuples, Lists and Dictionaries

## Tuple 

```
Tuple, bir kere tanımlandığında, elemanları değiştirilemeyen veri yapısıdır. Bu demektir ki, programın başında bir kere tanımlandıktan sonra içeriğini değiştirmek mümkün değildir. normal parantez ile gösterilir ().
```

## List 
```
Listlerin içeriği program sırasında değiştirilebilir, python'da veri depolamak için kullanılan en yaygın veri yapılarından birisidir. Listlerin depolanan değişkenlerin veri tipi aynı olmak zorunda değildir. Köşeli parantez ile gösterilir [].
```

## Dictionary

```
Key-value yapısı vardır. Key'e eriştiğimizde value'yu elde edebilirsiniz. Program sırasında değiştirilebilir. Süslü parantez ile gösterilir {}.
```

### Örnek -1 
#### meyveler içeren bir liste tanımlayalım.
```
meyveler = ["muz", "elma", "karpuz"]
```

#### listenin bir elemanına indexi ile ulaşma.
```
meyveler[0] # 'muz'
```

#### Listler iterable'dır. üzerinde indexlerini kullanarak hareket edebiliriz. 

```
for meyve in meyveler: 
    for harf in meyve:
        print(harf)
    print()
```

```
# listden indexini kullanarak bir eleman silme
del meyveler[2]
# listeye yeni bir eleman ekleme. 
meyveler.append("üzüm")
# listeyi sort etme (sıralamak - alfebatik)
print(sorted(meyveler)) # ['elma','muz','üzüm']
```

### Örnek - 2 
#### Tuple 
```
isim = ("Deniz", "Fatih", "Mert")

# tuple içindeki elemanın indeksine erişme.
isim.index("Cagla") # 0

new_tuple = ("Cagla", "Ali", "Cagla", "Önder")

# tuple içerisindeki belirli bir elemanın kaç kere tekrarlandığını döndürme.
new_tuple.count("Deniz") # 1
```

### Örnek - 3 
#### Dictionary
```
renkler = {
    1 : "kırmızı",
    2 : "sarı", 
    3 : "yeşil",
    "a" : "aaa"
}

print(renkler) # {1: 'kırmızı', 2: 'sarı', 3: 'yeşil', 'a': 'aaa'}


# dictionary içerisindeki tüm veriyi temizleme -> .clear()
renkler.clear()

renkler # {}

renkler["kırmızı"] = "red"
renkler["blue"] = "mavi"

renkler.keys() # dict_keys(['kırmızı', 'blue'])

renkler.items() # dict_items([('kırmızı', 'red'), ('blue', 'mavi')])

renkler.values() # dict_values(['red', 'mavi'])

# .get fonksiyonu ile dictionary içeriğine ulaşmak
renkler.get("kırmızı") # 'red'
```

### Karışık örnekler. 

#### listenin uzunluğuna erişme

```
meyveler = ["muz", "elma", "karpuz"]

print(len(meyveler)) # 3


meyveler[1:3] # ['elma', 'karpuz']

meyveler.append("üzüm")
meyveler.append("çilek")

meyveler # ['muz', 'elma', 'karpuz', 'üzüm', 'çilek']
```

#### liste içerisindeki elemanı kontrol etme. 
```
meyve = input("meyve: ")

if meyve in meyveler:
    print(meyve, " listede mevcut.")
else:
    meyveler.append(meyve)
    print(meyve, " listeye eklendi.")
    print(meyveler)
```
 
### Örnek - 4 
#### ülke isimleri içeren bir tuple oluştur. kullanıcıdan tuple'daki bir ülkenin ismini girmesini iste. girilen ülkenin indeksini göster. 
```
ulke  = ("Fransa", "Ingiltere", "Almanya", "Ispanya", "Romanya", "Turkiye")
print(ulke)
print()

choice = input("Yukarıdaki listeden bir ülke ismi giriniz. ")

if choice in ulke: 
    print(choice, "ülkeler listesinde ", ulke.index(choice) + 1,". sırada.")
else:
    print("Girilen ülke listede bulunmuyor.")

"""
('Fransa', 'Ingiltere', 'Almanya', 'Ispanya', 'Romanya', 'Turkiye')

Yukarıdaki listeden bir ülke ismi giriniz. Hollanda
Girilen ülke listede bulunmuyor.
"""
```


### Örnek - 5 

```
spor_dallari = ["futbol"] 

print("------Sınıfta ilgi duyulan sporlar anketi-------")
kisi_sayisi = int(input("Sınıfta kaç kişi mevcut? "))

for i in range(0,kisi_sayisi):
    print("Ankete hoş geldin!")
    print("Listede şu sporlar mevcut: ", spor_dallari)
    spor = input("Sen hangi spor dalına ilgi duyuyorsun?")
    
    if spor not in spor_dallari:
        spor_dallari.append(spor)
        
    print("Cevabın için teşekkürler.")
    print()

print("Sınıfta ilgi duyulan spor dalları şunlardır: ")
print(spor_dallari)
```

### Örnek - 6 
#### Pizzadan istemediğimiz yiyecekleri çıkartma menüsü.

```
"""
içindekiler listesi olmalı. user'a çıkartmak istediğin var mı diye sormalı, 
varsa o yiyeceği çıkartarak listenin son halini bastırmalı.
"""

icindekiler = ["mantar", "sosis", "yesil biber", "sucuk", "misir"]
pizza_boyut_fiyat_tablosu = {"küçük": 50, "orta": 75, "büyük":95 }

print("Pizzacıya hoş geldin! Pizzanın boyutu ne olsun?")
print(list(pizza_boyut_fiyat_tablosu.keys()))

secilen_boyut = input()

print("Pizzanın içinde olmasını istemediğiniz malzemeyi seçin: ")


for i in range(0, len(icindekiler)):
    print(i+1 ,": ", icindekiler[i])
istenmeyen_malzeme = int(input())

del icindekiler[istenmeyen_malzeme-1]

print("-------------------")
print("Siparişiniz alındı.")
print("Ödenecek tutar: ", pizza_boyut_fiyat_tablosu[secilen_boyut],"TL. " )
print("Pizza içeriği: ", icindekiler)
```

### Örnek - 7 

#### kullanıcı takip ettiği dizileri listeye eklesin. listeden bir tane örnek rastgele olarak kullanıcıya önerilsin. 
```
import random

dizi = []

print("Dizi önerme merkezine hoşgeldiniz. Listenizi oluşturmaya başlayın.")

cevap = "evet"

while cevap == "evet":
    yeni_dizi = input("Dizi adı: ")
    dizi.append(yeni_dizi)
    cevap = input("Başka dizi eklemek ister misiniz? (evet/hayıt)")

print("Dizi listeniz oluşturuldu. Listedeki diziler şöyle: ")
print(dizi)

print("Sizin için rastgele bir dizi öneriliyor...")

rastgele = random.choice(dizi)
print("Şansınıza ", rastgele, "çıktı. Keyifli seyirler!")
```

## 2D Lists & Dictionaries

```
notlar = [[10, 70, 50], [20, 10, 90], [70, 85, 100]]

notlar_dict = {
    "Ali": [10, 70, 50],
    "Veli": [20, 10, 90],
    "Zeynep":[70, 85, 100] 
}

notlar_dict2 = {
    #"Ali": [10, 70, 50],
    "Ali": {"1. Sınav": 10, "2. Sınav":70, "Final":50},
    "Veli": {"1. Sınav": 20, "2. Sınav":10, "Final":90},
    "Zeynep":{"1. Sınav": 70, "2. Sınav":85, "Final":100} 
}

notlar_dict2.keys() # dict_keys(['Ali', 'Veli', 'Zeynep'])

notlar_dict2["Ali"] # {'1. Sınav': 10, '2. Sınav': 70, 'Final': 50}

notlar_dict2["Ali"].keys() # dict_keys(['1. Sınav', '2. Sınav', 'Final'])

notlar_dict2["Ali"]["Final"] =  70

# diyelim ki sınıfa yeni birisi katıldı 
notlar_dict2["Cagla"] = {"1. Sınav": 45, "2. Sınav": 56, "Final":89}

# sınıftan birisi ayrıldı. 
del notlar_dict2["Zeynep"]

```

### Örnek - 8 


#### final notu 80'in altında olanlar sınıftan düşsün.

```
# iki sınıf oluşturalım. 
# final notu 80 altında olanlar 2. sınıfta olsun, üstünde olanlar 1. sınıfta olsun.

sinif1 = {}
sinif2 = {}

for ogrenci in notlar_dict2:
    if notlar_dict2[ogrenci]["Final"] < 80:
        sinif2[ogrenci] = notlar_dict2[ogrenci]
    else:
        sinif1[ogrenci] = notlar_dict2[ogrenci]

print("1. Sınıfa geçmeye hak kazananlar: ", list(sinif1.keys()))

print("2. Sınıfta kalanlar: ", list(sinif2.keys()))

# 1. Sınıfa geçmeye hak kazananlar:  ['Veli', 'Cagla', 'Betül']
# 2. Sınıfta kalanlar:  ['Ahmet', 'Ayşe']
```

### Örnek - 9 
#### Sınıftaki öğrencilerin bilgilerinin toplandığı liste.

```
# öğretmen öğrencilerin bilgilerini sisteme ekliyor
sinif_listesi = {}

print("12A Sınıfı, öğrenci bilgisi toplama sistemine hoşgeldiniz. ")
kisi_sayisi = int(input("Sınıfınızda kaç kişi mevcut?"))

for i in range(0,kisi_sayisi):
    isim = input("Ogrencinin ismi: ")
    numara = input("Ogrenci numarası: ")
    ders = input("En basarılı olduğu ders: ")
    
    #sinif_listesi[isim] = {"Numara":numara, "En sevdiği ders":ders}
    sinif_listesi[isim] = {}
    sinif_listesi[isim]["Numara"] = numara
    sinif_listesi[isim]["En sevdiği ders"] = ders
```

```
print("Öğrenci bilgi sistemine hoş geldiniz. Giriş yapmak için bilgilerinizi girin.")

isim = input("İsim: ")
numara = input("Numara: ")

if isim in sinif_listesi.keys() and sinif_listesi[isim]["Numara"] == numara:
    print("Başarılı giriş.")
    
    print("Öğrenciye ait bilgiler: ")
    print("İsim : ", isim)
    for bilgi in sinif_listesi[isim]:
        print(bilgi, " : ", sinif_listesi[isim][bilgi])
    
else: 
    print("Öğrenci bulunamadı.")
```

```
print("Sınav notlarını her öğrenci için giriniz: ")

for ogrenci in sinif_listesi:
    print("Öğrenci adı: ", ogrenci)
    sinav_1 = input("1. Sınav notu: ")
    sinif_listesi[ogrenci]["1. Sınav: "] = sinav_1
    
    sinav_2 = input("2. Sınav notu: ")
    sinif_listesi[ogrenci]["2. Sınav: "] = sinav_2
    
    final = input("Final notu: ")
    sinif_listesi[ogrenci]["Final: "] = final
```

```
print("Öğrenci bilgi sistemine hoş geldiniz. Giriş yapmak için bilgilerinizi girin.")

isim = input("İsim: ")
numara = input("Numara: ")

if isim in sinif_listesi.keys() and sinif_listesi[isim]["Numara"] == numara:
    print("Başarılı giriş.")
    
    print("Öğrenciye ait bilgiler: ")
    print("İsim : ", isim)
    for bilgi in sinif_listesi[isim]:
        print(bilgi, " : ", sinif_listesi[isim][bilgi])
    
else: 
    print("Öğrenci bulunamadı.")
```









