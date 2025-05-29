---
title: StructuredDocumentTag.Style
linktitle: Style
articleTitle: Style
second_title: .NET için Aspose.Words
description: Belgenizin biçimlendirmesini geliştirmek ve okunabilirliği zahmetsizce artırmak için StructuredDocumentTags'in Stil özelliğini nasıl yöneteceğinizi keşfedin.
type: docs
weight: 260
url: /tr/net/aspose.words.markup/structureddocumenttag/style/
---
## StructuredDocumentTag.Style property

Yapılandırılmış belge etiketinin Stilini alır veya ayarlar.

```csharp
public Style Style { get; set; }
```

## Notlar

Sadece Character stil veyaParagraph bağlantılı karakter stili ile stil ayarlanabilir.

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

* class [Style](../../../aspose.words/style/)
* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
