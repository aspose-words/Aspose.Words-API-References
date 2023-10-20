---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words for .NET
description: Aspose.Words.Markup.MarkupLevel Sıralama. Belge ağacında belirli bir öğenin bulunduğu düzeyi belirtir.StructuredDocumentTag oluşabilir C#'da.
type: docs
weight: 3980
url: /tr/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Belge ağacında belirli bir öğenin bulunduğu düzeyi belirtir.[`StructuredDocumentTag`](../structureddocumenttag/) oluşabilir.

```csharp
public enum MarkupLevel
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Unknown | `0` | Bilinmeyen veya geçersiz değeri belirtir. |
| Inline | `1` | Öğe satır içi düzeyde oluşur (örneğin metin dizileri arasında). |
| Block | `2` | Öğe blok düzeyinde oluşur (örn. tablolar ve paragraflar arasında). |
| Row | `3` | Öğe, tablodaki satırlar arasında bulunur. |
| Cell | `4` | Öğe, satırdaki hücreler arasında bulunur. |

## Örnekler

İçerik kontrol öğelerine ilişkin stillerle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda belgeden yapılandırılmış belge etiketine stil uygulamanın iki yolu verilmiştir.
// 1 - Belgenin stil koleksiyonundan bir stil nesnesi uygulayın:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Belgedeki bir stile ada göre referans verin:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
