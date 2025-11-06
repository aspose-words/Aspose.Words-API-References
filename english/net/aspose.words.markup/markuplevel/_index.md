---
title: MarkupLevel Enum
linktitle: MarkupLevel
articleTitle: MarkupLevel
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Markup.MarkupLevel enum, defining where StructuredDocumentTags fit in your document tree for enhanced organization and control.
type: docs
weight: 4700
url: /net/aspose.words.markup/markuplevel/
---
## MarkupLevel enumeration

Specifies the level in the document tree where a particular [`StructuredDocumentTag`](../structureddocumenttag/) can occur.

```csharp
public enum MarkupLevel
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Unknown | `0` | Specifies the unknown or invalid value. |
| Inline | `1` | The element occurs at the inline level (e.g. among as runs of text). |
| Block | `2` | The element occurs at the block level (e.g. among tables and paragraphs). |
| Row | `3` | The element occurs among rows in a table. |
| Cell | `4` | The element occurs among cells in a row. |

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

* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
