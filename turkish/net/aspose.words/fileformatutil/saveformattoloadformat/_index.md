---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: Aspose.Words for .NET
description: FileFormatUtil SaveFormatToLoadFormat yöntem. Biri dönüştürürSaveFormat bir değerLoadFormat mümkünse değer C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Bir'i dönüştürür[`SaveFormat`](../../saveformat/) bir değer[`LoadFormat`](../../loadformat/) mümkünse değer.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentException | Dönüştürülemediğinde atar. |

## Örnekler

Bir kaydetme biçiminin karşılık gelen yükleme biçimine nasıl dönüştürüleceğini gösterir.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Bazı dosya türlerinde belgeler Aspose.Words'e kaydedilebilir ancak Aspose.Words kullanılarak yüklenmeyebilir.
// Böyle bir kayıt biçimini yükleme biçimine dönüştürmeye çalışırsak bir istisna atılır.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Ayrıca bakınız

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
