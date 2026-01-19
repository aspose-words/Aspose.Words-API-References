---
title: CompositeNode.getText method
linktitle: getText method
articleTitle: getText method
second_title: Aspose.Words for Node.js
description: "CompositeNode.getText method. Gets the text of this node and of all its children."
type: docs
weight: 230
url: /nodejs-net/aspose.words/compositenode/getText/
---

## getText() {#default}

Gets the text of this node and of all its children.


```js
getText()
```

### Remarks

The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




### Examples

Shows the difference between calling the GetText and ToString methods on a node.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.insertField("MERGEFIELD Field");
// GetText will retrieve the visible text as well as field codes and special characters.
expect(doc.getText().trim()).toEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015");
// ToString will give us the document's appearance if saved to a passed save format.
expect(doc.toString(aw.SaveFormat.Text).trim()).toEqual("«Field»");
```

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
* class [CompositeNode](../)

