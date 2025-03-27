---
title: MarkupLevel enumeration
linktitle: MarkupLevel enumeration
articleTitle: MarkupLevel enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Markup.MarkupLevel enumeration. Specifies the level in the document tree where a particular [StructuredDocumentTag](../structureddocumenttag/) can occur."
type: docs
weight: 90
url: /nodejs-net/Aspose.Words.Markup/markuplevel/
---

## MarkupLevel enumeration

Specifies the level in the document tree where a particular [StructuredDocumentTag](../structureddocumenttag/) can occur.



### Members

| Name | Description |
| --- | --- |
| Unknown | Specifies the unknown or invalid value. |
| Inline | The element occurs at the inline level (e.g. among as runs of text). |
| Block | The element occurs at the block level (e.g. among tables and paragraphs). |
| Row | The element occurs among rows in a table. |
| Cell | The element occurs among cells in a row. |

### Examples

Shows how to work with styles for content control elements.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are two ways to apply a style from the document to a structured document tag.
// 1 -  Apply a style object from the document's style collection:
let quoteStyle = doc.styles.at(aw.StyleIdentifier.Quote);
let sdtPlainText = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Inline);
sdtPlainText.style = quoteStyle;

// 2 -  Reference a style in the document by name:
let sdtRichText = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.RichText, aw.Markup.MarkupLevel.Inline);
sdtRichText.styleName = "Quote";

builder.insertNode(sdtPlainText);
builder.insertNode(sdtRichText);

expect(sdtPlainText.nodeType).toEqual(aw.NodeType.StructuredDocumentTag);

let tags = doc.getChildNodes(aw.NodeType.StructuredDocumentTag, true);

for (let node of tags)
{
  let sdt = node.asStructuredDocumentTag();

  console.log(sdt.wordOpenXMLMinimal);

  expect(sdt.style.styleIdentifier).toEqual(aw.StyleIdentifier.Quote);
  expect(sdt.styleName).toEqual("Quote");
}
```

### See Also

* module [Aspose.Words.Markup](../)

