---
title: License.License
second_title: Aspose.Words for .NET API Referansı
description: License inşaatçı. Bu sınıfın yeni bir örneğini başlatır.
type: docs
weight: 10
url: /tr/net/aspose.words/license/license/
---
## License constructor

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public License()
```

### Örnekler

Yerel dosya sisteminde bir lisans dosyası kullanarak Aspose.Words için bir lisansın nasıl başlatılacağını gösterir.

```csharp
// Geçerli bir lisans dosyasının yerel dosya sistemi dosya adını ileterek Aspose.Words ürünümüz için lisansı ayarlayın.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Uygulamamızın binaries klasöründe lisans dosyamızın bir kopyasını oluşturun.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Bir dosyanın adını yolsuz iletirsek,
// SetLicense, bu dosya için birkaç yerel dosya sistemi konumunu arayacaktır.
// Bu konumlardan biri, lisans dosyamızın bir kopyasını içeren "bin" klasörü olacaktır.
license.SetLicense("Aspose.Words.NET.lic");
```

### Ayrıca bakınız

* class [License](../)
* ad alanı [Aspose.Words](../../license/)
* toplantı [Aspose.Words](../../../)


