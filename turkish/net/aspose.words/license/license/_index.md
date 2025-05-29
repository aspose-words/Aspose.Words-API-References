---
title: License
linktitle: License
articleTitle: License
second_title: .NET için Aspose.Words
description: Oluşturucu sınıfımızla lisansları zahmetsizce oluşturun ve yönetin. Lisanslama sürecinizi basitleştirin ve verimliliği bugün artırın!
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

Yerel dosya sistemindeki bir lisans dosyasını kullanarak Aspose.Words için bir lisansın nasıl başlatılacağını gösterir.

```csharp
// Aspose.Words ürünümüz için geçerli bir lisans dosyasının yerel dosya sistemi dosya adını geçirerek lisansı ayarlayın.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Uygulamamızın binaries klasöründe lisans dosyamızın bir kopyasını oluşturalım.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Eğer bir dosyanın adını yol olmadan geçirirsek,
// SetLicense bu dosyayı çeşitli yerel dosya sistemi konumlarında arayacaktır.
// Bu konumlardan biri, lisans dosyamızın bir kopyasını içeren "bin" klasörü olacaktır.
license.SetLicense("Aspose.Words.NET.lic");
```

### Ayrıca bakınız

* class [License](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
