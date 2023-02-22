---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
second_title: Aspose.Words for .NET API Referansı
description: JsonDataLoadOptions mülk. JSON yüklenirken JSON tarihsaat değerlerini ayrıştırmak için tam biçimleri alır veya ayarlar. Varsayılan hükümsüz .
type: docs
weight: 30
url: /tr/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

JSON yüklenirken JSON tarih-saat değerlerini ayrıştırmak için tam biçimleri alır veya ayarlar. Varsayılan **hükümsüz** .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

### Notlar

Microsoft® JSON tarih-saat biçimi (örneğin, "/Date(1224043200000)/") kullanılarak kodlanan dizeler, bu özelliğin değerinden bağımsız olarak her zaman tarih-saat değerleri olarak tanınır. Özellik, dizelerden tarih-saat değerleri ayrıştırılırken kullanılacak ek biçimlerini şu şekilde tanımlar:

* Ne zaman`ExactDateTimeParseFormats` dır-dir **hükümsüz** , geçerli, İngilizce ABD ve İngiliz Yeni Zelanda kültürleri için desteklenen ISO-8601 biçimi ve tüm tarih-saat biçimleri ek olarak belirtilen sırada içinde kullanılır.
* Ne zaman`ExactDateTimeParseFormats` dizeler içerir, geçerli kültürü kullanan ek tarih-saat biçimleri olarak kullanılırlar.
* Ne zaman`ExactDateTimeParseFormats` boşsa, ek tarih-saat biçimi kullanılmaz.

### Ayrıca bakınız

* class [JsonDataLoadOptions](../)
* ad alanı [Aspose.Words.Reporting](../../jsondataloadoptions/)
* toplantı [Aspose.Words](../../../)


