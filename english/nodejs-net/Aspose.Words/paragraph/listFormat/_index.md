---
title: Paragraph.listFormat property
linktitle: listFormat property
articleTitle: listFormat property
second_title: Aspose.Words for Node.js
description: "Paragraph.listFormat property. Provides access to the list formatting properties of the paragraph."
type: docs
weight: 150
url: /nodejs-net/aspose.words/paragraph/listFormat/
---

## Paragraph.listFormat property

Provides access to the list formatting properties of the paragraph.


```js
get listFormat(): Aspose.Words.Lists.ListFormat
```

### Examples

Shows how to output all paragraphs in a document that are list items.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.listFormat.applyNumberDefault();
builder.writeln("Numbered list item 1");
builder.writeln("Numbered list item 2");
builder.writeln("Numbered list item 3");
builder.listFormat.removeNumbers();

builder.listFormat.applyBulletDefault();
builder.writeln("Bulleted list item 1");
builder.writeln("Bulleted list item 2");
builder.writeln("Bulleted list item 3");
builder.listFormat.removeNumbers();

let nodes = [...doc.getChildNodes(aw.NodeType.Paragraph, true)];

for (let node of nodes.filter(p => p.asParagraph().listFormat.isListItem))
{ 
  var para = node.asParagraph();
  console.log(`This paragraph belongs to list ID# ${para.listFormat.list.listId}, number style \"${para.listFormat.listLevel.numberStyle}\"`);
  console.log(`\t\"${para.getText().trim()}\"`);
}
```

### See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

