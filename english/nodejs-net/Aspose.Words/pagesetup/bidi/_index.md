---
title: PageSetup.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Node.js
description: "PageSetup.bidi property. Specifies that this section contains bidirectional (complex scripts) text."
type: docs
weight: 10
url: /nodejs-net/aspose.words/pagesetup/bidi/
---

## PageSetup.bidi property

Specifies that this section contains bidirectional (complex scripts) text.


```js
get bidi(): boolean
```

### Remarks

When ``true``, the columns in this section are laid out from right to left.




### Examples

Shows how to set the order of text columns in a section.

```js
let doc = new aw.Document();

let pageSetup = doc.sections.at(0).pageSetup;
pageSetup.textColumns.setCount(3);

let builder = new aw.DocumentBuilder(doc);
builder.write("Column 1.");
builder.insertBreak(aw.BreakType.ColumnBreak);
builder.write("Column 2.");
builder.insertBreak(aw.BreakType.ColumnBreak);
builder.write("Column 3.");

// Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
// The order of the columns will match the direction of the right-to-left text.
// Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
// The order of the columns will match the direction of the left-to-right text.
pageSetup.bidi = reverseColumns;

doc.save(base.artifactsDir + "PageSetup.bidi.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

