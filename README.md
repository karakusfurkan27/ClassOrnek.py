## README - Okul Sınıfı Örneği  

Bu proje, Python programlama dilinde bir sınıf (`class`) kullanarak basit bir nesne yönelimli programlama örneği sunmaktadır. Kodda bir `Okul` sınıfı tanımlanmış ve bu sınıf üzerinden iki nesne (`p1` ve `p2`) oluşturulmuştur. Nesneler, öğrencilerin isim ve yaş bilgilerini saklamak için kullanılmıştır.

---

### Kodun Çalışma Prensibi  

1. **Sınıf Tanımı:**  
   `Okul` adında bir sınıf tanımlanmış ve sınıfa iki adet özellik (attribute) eklenmiştir:  
   - `namme`: Öğrencinin adı (varsayılan olarak boş bir string)  
   - `age`: Öğrencinin yaşı (varsayılan olarak `0`)  

2. **Nesne Oluşturma ve Özellik Atama:**  
   - `p1` ve `p2` adında iki nesne oluşturulmuştur.  
   - Her bir nesneye `namme` ve `age` özellikleri atanmıştır.  

3. **Bilgi Yazdırma:**  
   - Her bir nesne için öğrencinin adı ve yaşı f-string formatında yazdırılmıştır.  

---

### Kod

```python
class Okul:

    namme = ""
    age = 0

p1 = Okul()
p1.namme= "Berk"
p1.age = 22

p2 = Okul()
p2.namme= "Levent"
p2.age= 19

print(f"{p1.namme} {p1.age} yasindadir")
print(f"{p2.namme} {p2.age} yasindadir")
```

---

### Çıktı  

Kod çalıştırıldığında şu çıktı alınacaktır:  

```
Berk 22 yasindadir
Levent 19 yasindadir
```

---

### Önemli Notlar  

1. **Yazım Hatası (`namme`):**  
   `Okul` sınıfında `name` yerine yanlışlıkla `namme` yazılmıştır. Daha doğru bir isimlendirme için `namme` yerine `name` kullanılabilir.  

2. **Sınıf Özellikleri:**  
   - `namme` ve `age` değişkenleri, sınıfın genel özellikleridir. Ancak her nesneye özgü özellikler (`instance attributes`) olarak tanımlanırsa daha temiz bir kod elde edilir.  

Örneğin:  
```python
class Okul:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

3. **Geliştirme Önerisi:**  
   - Kodda bir `__init__` metodu kullanılarak nesne oluşturma süreci daha düzenli hale getirilebilir.  
   - Örneğin:  
     ```python
     p1 = Okul("Berk", 22)
     p2 = Okul("Levent", 19)
     ```  

Bu README dosyası, kodun nasıl çalıştığını anlamanıza ve iyileştirme yapmanıza yardımcı olacaktır. 
