---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
linktitle: AdjustSentenceAndWordSpacing
articleTitle: AdjustSentenceAndWordSpacing
second_title: .NET için Aspose.Words
description: ImportFormatOptions AdjustSentenceAndWordSpacing özelliğini keşfedin. Gelişmiş metin netliği için otomatik cümle ve kelime aralığını kolayca kontrol edin.
type: docs
weight: 20
url: /tr/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

Cümle ve kelime aralıklarının otomatik olarak ayarlanıp ayarlanamayacağını belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

## Örnekler

Cümle ve kelime aralıklarının otomatik olarak nasıl ayarlanacağını gösterir.

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
