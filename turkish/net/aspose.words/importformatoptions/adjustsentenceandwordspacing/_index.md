---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
second_title: Aspose.Words for .NET API Referansı
description: ImportFormatOptions mülk. Cümle ve kelime aralığının otomatik olarak ayarlanıp ayarlanmayacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değerYANLIŞ .
type: docs
weight: 20
url: /tr/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

Cümle ve kelime aralığının otomatik olarak ayarlanıp ayarlanmayacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` .

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

### Örnekler

Cümle ve sözcük aralığının otomatik olarak nasıl ayarlanacağını gösterir.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(srcDoc);
builder.Write("Dolor sit amet.");

builder = new DocumentBuilder(dstDoc);
builder.Write("Lorem ipsum.");

ImportFormatOptions options = new ImportFormatOptions() { AdjustSentenceAndWordSpacing = true };
builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

Assert.AreEqual("Lorem ipsum. Dolor sit amet.", dstDoc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Ayrıca bakınız

* class [ImportFormatOptions](../)
* ad alanı [Aspose.Words](../../importformatoptions/)
* toplantı [Aspose.Words](../../../)


