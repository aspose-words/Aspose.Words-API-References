---
title: ParagraphFormat.BaselineAlignment
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Yazı tiplerinin bir satırdaki dikey konumunu alır veya ayarlar.
type: docs
weight: 40
url: /tr/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Yazı tiplerinin bir satırdaki dikey konumunu alır veya ayarlar.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

### Örnekler

Yazı tiplerinin bir satırdaki dikey konumunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### Ayrıca bakınız

* enum [BaselineAlignment](../../baselinealignment/)
* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


