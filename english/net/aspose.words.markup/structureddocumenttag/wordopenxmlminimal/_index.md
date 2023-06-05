---
title: StructuredDocumentTag.WordOpenXMLMinimal
linktitle: WordOpenXMLMinimal
articleTitle: WordOpenXMLMinimal
second_title: Aspose.Words for .NET
description: StructuredDocumentTag WordOpenXMLMinimal property. Gets a string that represents the XML contained within the node in the FlatOpc format. Unlike the WordOpenXML property this method generates a strippeddown document that excludes any noncontentrelated parts in C#.
type: docs
weight: 310
url: /net/aspose.words.markup/structureddocumenttag/wordopenxmlminimal/
---
## StructuredDocumentTag.WordOpenXMLMinimal property

Gets a string that represents the XML contained within the node in the FlatOpc format. Unlike the [`WordOpenXML`](../wordopenxml/) property, this method generates a stripped-down document that excludes any non-content-related parts.

```csharp
public string WordOpenXMLMinimal { get; }
```

## Examples

Shows how to work with styles for content control elements.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two ways to apply a style from the document to a structured document tag.
// 1 -  Apply a style object from the document's style collection:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 -  Reference a style in the document by name:
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

### See Also

* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../structureddocumenttag/)
* assembly [Aspose.Words](../../../)
