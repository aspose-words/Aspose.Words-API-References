---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: .NET için Aspose.Words
description: SaveFormat'ı FileFormatUtil yöntemiyle zahmetsizce LoadFormat'a dönüştürün. Dosya yönetimini basitleştirin ve uyumluluğu bugün artırın!
type: docs
weight: 90
url: /tr/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Birini dönüştürür[`SaveFormat`](../../saveformat/) bir değere[`LoadFormat`](../../loadformat/) mümkünse değer.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentException | Dönüştürülemediğinde atar. |

## Örnekler

Bir kayıt formatının karşılık gelen yükleme formatına nasıl dönüştürüleceğini gösterir.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Bazı dosya türlerine belgeler kaydedilebilir, ancak Aspose.Words kullanılarak bu dosyalardan yüklenemez.
// Bu tür bir kayıt formatını yükleme formatına dönüştürmeye çalışırsak bir istisna atılır.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Ayrıca bakınız

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
