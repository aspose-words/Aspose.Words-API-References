---
title: StructuredDocumentTag.wordOpenXMLMinimal property
linktitle: wordOpenXMLMinimal property
articleTitle: wordOpenXMLMinimal property
second_title: Aspose.Words for Node.js
description: "StructuredDocumentTag.wordOpenXMLMinimal property. Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../../aspose.words/saveformat/#FlatOpc) format."
type: docs
weight: 310
url: /nodejs-net/aspose.words.markup/structureddocumenttag/wordOpenXMLMinimal/
---

## StructuredDocumentTag.wordOpenXMLMinimal property

Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../../aspose.words/saveformat/#FlatOpc) format.

Unlike the [StructuredDocumentTag.wordOpenXML](../wordOpenXML/) property, this method generates a stripped-down document that excludes any non-content-related parts.



```js
get wordOpenXMLMinimal(): string
```

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

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTag](../)

