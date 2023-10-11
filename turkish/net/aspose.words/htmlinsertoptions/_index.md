---
title: Enum HtmlInsertOptions
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.HtmlInsertOptions Sıralama. Şunun için seçenekleri belirtirInsertHtml yöntem.
type: docs
weight: 3140
url: /tr/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

Şunun için seçenekleri belirtir:[`InsertHtml`](../documentbuilder/inserthtml/) yöntem.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | HTML'yi eklerken varsayılan seçenekleri kullanın. |
| UseBuilderFormatting | `1` | Belirtilen yazı tipi ve paragraf formatını kullan[`DocumentBuilder`](../documentbuilder/) HTML. 'den eklenen text için temel biçimlendirme olarak |
| RemoveLastEmptyParagraph | `2` | Normalde HTML'den sonra eklenen ve blok düzeyinde bir öğeyle biten boş paragrafı kaldırın. |
| PreserveBlocks | `4` | Blok düzeyindeki öğelerin özelliklerini koruyun. |

### Örnekler

Görünen kenarlıkların ve kenar boşluklarının daha iyi korunmasına nasıl izin verileceğini gösterir.

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

// HTML blok düzeyindeki öğelerin içe aktarılmasının yeni modunu ayarlayın.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


