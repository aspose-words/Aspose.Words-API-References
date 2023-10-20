---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words for .NET
description: Aspose.Words.BaselineAlignment Sıralama. Yazı tiplerinin bir satırdaki dikey konumunu belirtir C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

Yazı tiplerinin bir satırdaki dikey konumunu belirtir.

```csharp
public enum BaselineAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Top | `0` | Her yazı tipinin üst kısmı boyunca hizalar. |
| Center | `1` | Her yazı tipinin merkez noktalarını hizalar. |
| Baseline | `2` | Paragrafın taban çizgisine hizalar. |
| Bottom | `3` | Her yazı tipinin alt kısmına hizalar. |
| Auto | `4` | Taban çizgisi otomatik olarak ayarlanır. |

## Örnekler

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
