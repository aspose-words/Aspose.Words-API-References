---
title: License Class
linktitle: License
articleTitle: License
second_title: .NET için Aspose.Words
description: Lisans sınıfımızla Aspose.Words'ün tüm potansiyelini açığa çıkarın. Sorunsuz belge işleme ve gelişmiş işlevsellik için lisanslamayı kolayca yönetin.
type: docs
weight: 3870
url: /tr/net/aspose.words/license/
---
## License class

Bileşeni lisanslamak için yöntemler sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Lisanslama ve Abonelik](https://docs.aspose.com/words/net/licensing/) belgeleme makalesi.

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
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(*Stream*) | Bileşeni lisanslar. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(*string*) | Bileşeni lisanslar. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
