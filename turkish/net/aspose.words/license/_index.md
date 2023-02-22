---
title: Class License
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.License sınıf. Bileşeni lisanslamak için yöntemler sağlar.
type: docs
weight: 3220
url: /tr/net/aspose.words/license/
---
## License class

Bileşeni lisanslamak için yöntemler sağlar.

```csharp
public class License
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [License](license/)() | Bu sınıfın yeni bir örneğini başlatır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(Stream) | Bileşeni lisanslar. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(string) | Bileşeni lisanslar. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


