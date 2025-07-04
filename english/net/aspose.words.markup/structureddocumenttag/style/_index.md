---
title: StructuredDocumentTag.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words for .NET
description: Discover how to manage the Style property of StructuredDocumentTags to enhance your document formatting and improve readability effortlessly.
type: docs
weight: 260
url: /net/aspose.words.markup/structureddocumenttag/style/
---
## StructuredDocumentTag.Style property

Gets or sets the Style of the structured document tag.

```csharp
public Style Style { get; set; }
```

## Remarks

Only Character style or Paragraph style with linked character style can be set.

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

Assert.That(sdtPlainText.NodeType, Is.EqualTo(NodeType.StructuredDocumentTag));

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.That(sdt.Style.StyleIdentifier, Is.EqualTo(StyleIdentifier.Quote));
    Assert.That(sdt.StyleName, Is.EqualTo("Quote"));
}
```

### See Also

* class [Style](../../../aspose.words/style/)
* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
