# Plakaya Göre İl ve İlçe Listesi Türkiye

Türkiye'deki tüm il ve ilçeleri listeleyen bir PHP Yapısı. İllere plaka numaraları üzerinden kolayca erişebilir ve o ildeki ilçeleri görüntüleyebilirsiniz.

## Özellikler

- Tüm Türkiye illeri ve ilçeleri listelenmiştir.
- İllere plaka numaraları ile erişim sağlanabilir.
- Kolay ve hızlı bir şekilde kullanabileceğiniz basit bir yapıdır kendi projeleriniz için rahatlıkla kullanabilirsinz.

### Örnek Kullanım

```php
<?php
include 'plakailceil.php'; //PHP Dosyamızı include ettik

$plaka = 1; // Adana için örnek plaka numarası

if (array_key_exists($plaka, $data)) {
    $il = $data[$plaka][0];
    $ilceler = $data[$plaka][1];

    echo "Seçilen İl: $il\n";
    echo "İlçeler:\n";
    foreach ($ilceler as $ilce) {
        echo "- $ilce\n";
    }
} else {
    echo "Geçerli bir plaka numarası girin.";
}
```

<h2>Örnek Çıktı</h2>
<pre>
<h4>Seçilen İl: Adana </h4>
<h4>İlçeler:</h4> 
- Aladağ
- Ceyhan
- Çukurova
- Feke
- İmamoğlu
- Karaisalı
- Karataş
- Kozan
- Pozantı
- Saimbeyli
- Sarıçam
- Seyhan
- Tufanbeyli
- Yumurtalık
- Yüreğir
</pre>
