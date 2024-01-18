# Python'a Giriş

## Yorum Satırı 

```
# yorum satırı

print(1)
```

```
"""
Çoklu yorum satırı
birden fazla satırlar için.
"""

print(1)
```

```
'''
Çoklu yorum satırı
birden fazla satırlar için.
Tek tırnaklı çoklu yorum satırı
'''

print(1)
```

## Değişken Tanımlama

```
number = 2 # integer

print(number)  # --> 2

number2 = 2.5 #float

print(number2) # --> 2.5


text = "Python 101 Eğitimi" #string 

print(text) # --> Python 101 Eğitimi


text = 7 

print(text) # --> 7 
```

## Değişkenleri Kullanma


```
num1 = 10
num2 = 8

answer = num1 + num 2

print(answer) # --> 18

answer = num1 - num2
print(answer) # --> 2

answer = num1*num2
print(answer) # --> 80

answer = num1 / num2
print(answer) # --> 1.25

answer = num1 // num2
print(answer) # --> 1
```

## Print Fonksiyonu 

```
    print("Print yapısı") # --> Print Yapısı

    print("birinci satır \nikinci satır") 
    # --> birinci satır
          ikinci satır

    print("Cevap: ",answer) # --> Cevap: 1

    print("Cevap: ",answer, "olarak bulundu.") # --> Cevap: 1 olarak bulundu.

    text = input("Bir kelime girin: ") # --> Bir kelime girin: deniz

    print("Hoşgeldin", text) # --> Hoşgeldin deniz

    num1 = int(input("Bir sayı girin.")) # --> Bir sayı girin: 1
    num2 = int(input("Diğer sayıyı girin.")) # --> Diğer sayıyı girin: 2

    toplam = num1 + num2

    print(toplam) # --> 3

    print(num1, "sayısından", num2, "sayısını çıkarttığımızda sonuç: ", num1-num2) # --> 1 sayısından 2 sayısını çıkarttığımızda sonuç: -1

    hesap = int(input("Hesap: ")) # --> Hesap: 200
    kisi_sayisi = int(input("Kaç kişisiniz?")) # --> Kaç kişisiniz: 5

    kisi_basi = hesap / kisi_sayisi

    print("Kişi başına düşen miktar: ", kisi_basi) # --> Kişi başına düşen miktar: 40

```


## Karar yapıları (İf-elif-else)
```
    num = 13

    if num > 10:
        print("Bu sayı ondan büyüktür.")
    else:
        print("Bu sayı ondan küçüktür.")

    # --> Bu sayı ondan büyüktür. 


    sayi = int(input("Bir sayı giriniz. "))
    #--> sayi : 12

    if sayi > 10:  # sayinin 10'dan büyük olduğu tüm durumlar
        print("10'dan büyük.")
        sayi2 = int(input("diğer sayiyi girin. ")) # --> sayi2: 6 
        print("iki sayının toplamı: ", sayi + sayi2)

    elif sayi == 10: # sayinin 10'a eşit olduğu durumlar.
        print("10'a eşit.")
        sayi2 = int(input("diğer sayiyi girin. "))
        print("ikinci sayının 10'a bölümü: ", sayi2 / sayi)

    else: # sayinin 10'dan büyük olmadığı tüm durumlar. 
        print("10'dan küçük. ")
        print("Tekrar dene. ")
    
    #--> Bu iki sayının toplamı: 18


    num = int(input("10 ile 20 aralığında bir sayı gir: "))

    if num >= 10 and num <= 20:
        print("Teşekkürler. ")
    else: 
        print("Girdiğin sayı aralık dışında.")

    # --> 10 ile 20 aralığında bir sayı gir: 34
          Girdiğin sayı aralık dışında.
    
    num = int(input("1 ile 5 arasında bir çift sayı giriniz. ")) # 2,4

    if num == 2 or num == 4:
        print("Sayı uygun. ")
    else:
        print("Yanlış.")

    age = int(input("Yaşınızı girin: "))

    # oy verme yaşı -> 18
    # motor ehliyeti alma yaşı -> 17
    # millet vekili olma yaşı: 22 
    
    if age >= 18:
        print("Oy verebilirsin.")
    elif age == 17:
        print("Motor ehliyeti alabilirsin.")
    else:
        print("Yaşın", age, "hiçbir açıklama bulunmuyor.")
        
    if age >=22:
            print("Aynı zamanda millet vekili de olabilirsin.")

    # --> Yaşınızı girin: 15
          Yaşın 15 hiçbir açıklama bulunmuyor.

    
    """
    if içerisinde kullanılabiliecek karşılaştırma ifadeleri
    1.  == (eşitlik kontrol eder.) 
    2. != (eşit olmamayı kontrol eder.)
    3. < (küçük olmayı kontrol eder.)
    4. > (büyüklük kontrol eder.)
    5. <= (küçük ve eşit olmayı kontrol eder.)
    6. >= (büyük ve eşit olmayı kontrol eder.)


    if içerisinde kullanılabilen lojik ifadeler
    1. and (and'in iki tarafında yazılan tüm durumların doğru olduğu durumda True döner.)
    2. or (or'un iki tarafından herhangi birisinin doğru olduğu durumda True döner.)
    """

```

## String

```
    name = input("İsminizi girin: ") #deniz
    age = input("Yaşınızı girin: ") # 20
    customer_id = name + age

    print(customer_id)

    # --> deniz20

    "deniz" * 2  # --> denizdeniz

    text = "deniz ök"
    len(text) # --> 8

    text.upper() # --> 'DENIZ OK'
    text.lower() # --> 'deniz ok'

    text.capitalize() # --> 'Deniz ok'

    text2 = "--Bu bir yazı.--"

    print(text2.strip("--")) # --> Bu bir yazı.

    text3 = "Python101"

    text3[3:6] # --> 'hon'
    text3[:6] # --> 'Python'

    text = "Deniz Ök \"Pamukkale üniversitesinde okuyorum.\" dedi."

    print(text)

    # --> Deniz Ök "Pamukkale üniversitesinde okuyorum." dedi.

    text2 = 'Python 101\'de öğrendiğim konu.'

    print(text2) # --> text2 = "Python 101'de öğrendiğim konu."
```


## Math Operations

```
import math

math.sqrt(9) # --> 3

math.pi # --> 3.141592653589793

round(pi,2) # --> 3.14

# Çember alanı hesaplama

# alan -> pi*r^2
# cevre -> 2pi*r

yari_cap = int(input("Yarıçap:"))
alan = math.pi * (yari_cap ** 2)
cevre = 2 * math.pi * yari_cap
print("Alan:",alan)
print("Cevre:",cevre)


"""
--> Yarıçap:5
    Alan: 78.53981633974483
    Cevre: 31.41592653589793
"""

2**2 # --> 4

math.pow(2,3) # --> 8.0

math.factorial(5) # 5! -> 5*4*3*2*1 --> 120

# En büyük ortak bölen (greatest common divisor)
math.gcd(24,72) # --> 24 

math.ceil(3.1) # --> 4

math.floor(3.9999999) # --> 3

# En küçük ortak kat. 
math.lcm(12,18) # --> 36

```









