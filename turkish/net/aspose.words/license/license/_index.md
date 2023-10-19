---
title: License
linktitle: License
articleTitle: License
second_title: Aspose.Words for .NET
description: License inşaatçı. Bu sınıfın yeni bir örneğini başlatır C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/license/license/
---
## License constructor

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public License()
```

## Örnekler

Yerel dosya sistemindeki bir lisans dosyasını kullanarak Aspose.Words lisansının nasıl başlatıldığını gösterir.

```csharp
// Geçerli bir lisans dosyasının yerel dosya sistemi dosya adını ileterek Aspose.Words ürünümüzün lisansını ayarlayın.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Uygulamamızın ikili dosyalar klasöründe lisans dosyamızın bir kopyasını oluşturun.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Bir dosyanın adını yol olmadan aktarırsak,
// SetLicense bu dosya için çeşitli yerel dosya sistemi konumlarını arayacaktır.
// Bu konumlardan biri lisans dosyamızın bir kopyasını içeren "bin" klasörü olacaktır.
license.SetLicense("Aspose.Words.NET.lic");
```

### Ayrıca bakınız

* class [License](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
