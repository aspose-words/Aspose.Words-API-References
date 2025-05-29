---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: .NET için Aspose.Words
description: Metninizin okunabilirliğini ve tasarımını geliştiren, nokta cinsinden hassas satır aralığı sağlayan Font LineSpacing özelliğini keşfedin.
type: docs
weight: 190
url: /tr/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Bu yazı tipinin satır aralığını (nokta cinsinden) döndürür.

```csharp
public double LineSpacing { get; }
```

## Örnekler

Bir yazı tipinin satır aralığının nokta cinsinden nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder için farklı yazı tipleri ayarlayın ve satır aralıklarını doğrulayın.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
