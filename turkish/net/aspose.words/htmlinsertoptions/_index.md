---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: .NET için Aspose.Words
description: Belge işleme verimliliğini artırmak için InsertHtml yöntemiyle HTML eklemeyi özelleştirmek üzere Aspose.Words.HtmlInsertOptions enum'unu keşfedin.
type: docs
weight: 3570
url: /tr/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Aşağıdakiler için seçenekleri belirtir:[`InsertHtml`](../documentbuilder/inserthtml/) yöntem.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | HTML eklerken varsayılan seçenekleri kullanın. |
| UseBuilderFormatting | `1` | Belirtilen yazı tipini ve paragraf biçimlendirmesini kullanın[`DocumentBuilder`](../documentbuilder/) HTML'den eklenen text için temel biçimlendirme olarak. |
| RemoveLastEmptyParagraph | `2` | Normalde blok düzeyindeki bir öğeyle biten HTML'den sonra eklenen boş paragrafı kaldırın. |
| PreserveBlocks | `4` | Blok düzeyindeki öğelerin özelliklerini koru. |

## Örnekler

Görülen sınırların ve kenar boşluklarının daha iyi korunmasına nasıl olanak tanınacağını gösterir.

```csharp
const string html = @"
    <html>
        <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
        </div>
    </html>";

// HTML blok düzeyindeki öğelerin içe aktarılması için yeni modu ayarlayın.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
