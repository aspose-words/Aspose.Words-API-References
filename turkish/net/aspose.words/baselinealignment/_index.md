---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: .NET için Aspose.Words
description: Hassas yazı tipi konumlandırması için Aspose.Words.BaselineAlignment enum'unu keşfedin. Belge biçimlendirmenizi en uygun dikey hizalama seçenekleriyle geliştirin.
type: docs
weight: 130
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
| Top | `0` | Her yazı tipinin üst kısmına hizalanır. |
| Center | `1` | Her yazı tipinin merkez noktalarını hizalar. |
| Baseline | `2` | Paragrafın temel çizgisine hizalanır. |
| Bottom | `3` | Her yazı tipinin altına hizalanır. |
| Auto | `4` | Temel çizgi otomatik olarak ayarlanır. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
