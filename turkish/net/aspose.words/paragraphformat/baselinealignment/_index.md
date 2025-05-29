---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: .NET için Aspose.Words
description: ParagraphFormat BaselineAlignment özelliğiyle metin düzeninizi optimize edin; bu sayede yazı tipi dikey konumlandırması üzerinde hassas kontrol sağlayarak okunabilirliği artırın.
type: docs
weight: 40
url: /tr/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Yazı tiplerinin bir satırdaki dikey konumunu alır veya ayarlar.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

## Örnekler

Bir satırda yazı tiplerinin dikey konumunun nasıl ayarlanacağını gösterir.

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
