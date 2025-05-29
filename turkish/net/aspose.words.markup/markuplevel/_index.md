---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: .NET için Aspose.Words
description: Gelişmiş organizasyon ve kontrol için StructuredDocumentTags'in belge ağacınızda nereye yerleştirileceğini tanımlayan Aspose.Words.Markup.MarkupLevel enum'unu keşfedin.
type: docs
weight: 4670
url: /tr/net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Belirli bir belgenin bulunduğu belge ağacındaki düzeyi belirtir.[`StructuredDocumentTag`](../structureddocumenttag/) meydana gelebilir.

```csharp
public enum MarkupLevel
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Unknown | `0` | Bilinmeyen veya geçersiz değeri belirtir. |
| Inline | `1` | Öğe satır içi düzeyde (örneğin metin çalıştırmaları arasında) oluşur. |
| Block | `2` | Öğe blok düzeyinde (örneğin tablolar ve paragraflar arasında) meydana gelir. |
| Row | `3` | Öğe bir tablonun satırları arasında yer alır. |
| Cell | `4` | Öğe bir satırdaki hücreler arasında meydana gelir. |

## Örnekler

İçerik kontrol öğeleri için stillerle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, bir belgeden yapılandırılmış belge etiketine bir stil uygulamanın iki yolu bulunmaktadır.
// 1 - Belgenin stil koleksiyonundan bir stil nesnesi uygula:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Belgedeki bir stile adıyla başvuruda bulunun:
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
