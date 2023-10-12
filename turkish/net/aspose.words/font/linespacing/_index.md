---
title: Font.LineSpacing
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Bu yazı tipinin satır aralığını döndürür nokta cinsinden.
type: docs
weight: 190
url: /tr/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Bu yazı tipinin satır aralığını döndürür (nokta cinsinden).

```csharp
public double LineSpacing { get; }
```

### Örnekler

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
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


