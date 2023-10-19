---
title: StructuredDocumentTag.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words for .NET
description: StructuredDocumentTag WordOpenXMLMinimal mülk. Düğümdeki düğümün içerdiği XMLi temsil eden bir dize alır.FlatOpc format. Şunun aksineWordOpenXMLözelliğinden yararlanarak bu yöntem içerikle ilgili olmayan bölümleri hariç tutan sadeleştirilmiş bir belge oluşturur C#'da.
type: docs
weight: 310
url: /tr/net/aspose.words.markup/structureddocumenttag/wordopenxmlminimal/
---
## StructuredDocumentTag.WordOpenXMLMinimal property

Düğümdeki düğümün içerdiği XML'i temsil eden bir dize alır.FlatOpc format. Şunun aksine[`WordOpenXML`](../wordopenxml/)özelliğinden yararlanarak, bu yöntem, içerikle ilgili olmayan bölümleri hariç tutan sadeleştirilmiş bir belge oluşturur.

```csharp
public string WordOpenXMLMinimal { get; }
```

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

* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
