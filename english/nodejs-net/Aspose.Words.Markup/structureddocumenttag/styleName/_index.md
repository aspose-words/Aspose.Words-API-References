---
title: StructuredDocumentTag.styleName property
linktitle: styleName property
articleTitle: styleName property
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTag.styleName property. Gets or sets the name of the style applied to the structured document tag."
type: docs
weight: 270
url: /nodejs-net/Aspose.Words.Markup/structureddocumenttag/styleName/
---

## StructuredDocumentTag.styleName property

Gets or sets the name of the style applied to the structured document tag.


```js
get styleName(): string
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

