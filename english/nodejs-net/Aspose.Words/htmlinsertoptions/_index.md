---
title: HtmlInsertOptions enumeration
linktitle: HtmlInsertOptions enumeration
articleTitle: HtmlInsertOptions enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.HtmlInsertOptions enumeration. Specifies options for the [DocumentBuilder.insertHtml()](../documentbuilder/insertHtml/#string_htmlinsertoptions) method."
type: docs
weight: 520
url: /nodejs-net/Aspose.Words/htmlinsertoptions/
---

## HtmlInsertOptions enumeration

Specifies options for the [DocumentBuilder.insertHtml()](../documentbuilder/insertHtml/#string_htmlinsertoptions) method.



### Members

| Name | Description |
| --- | --- |
| None | Use the default options when inserting HTML. |
| UseBuilderFormatting | Use font and paragraph formatting specified in [DocumentBuilder](../documentbuilder/) as base formatting for text inserted from HTML. |
| RemoveLastEmptyParagraph | Remove the empty paragraph that is normally inserted after HTML that ends with a block-level element. |
| PreserveBlocks | Preserve properties of block-level elements. |

### Examples

Shows how to allows better preserve borders and margins seen.

```js
const html = `
  <html>
    <div style='border:dotted'>
    <div style='border:solid'>
      <p>paragraph 1</p>
      <p>paragraph 2</p>
    </div>
    </div>
  </html>`;

// Set the new mode of import HTML block-level elements.
let insertOptions = aw.HtmlInsertOptions.PreserveBlocks;

let builder = new aw.DocumentBuilder();
builder.insertHtml(html, insertOptions);
builder.document.save(base.artifactsDir + "DocumentBuilder.preserveBlocks.docx");
```

### See Also

* module [Aspose.Words](../)

