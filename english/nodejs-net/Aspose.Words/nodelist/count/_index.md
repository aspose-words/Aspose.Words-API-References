---
title: NodeList.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for NodeJs
description: "NodeList.count property. Gets the number of nodes in the list."
type: docs
weight: 10
url: /nodejs-net/aspose.words/nodelist/count/
---

## NodeList.count property

Gets the number of nodes in the list.


```js
get count(): number
```

### Examples

Shows how to use XPaths to navigate a NodeList.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert some nodes with a DocumentBuilder.
builder.writeln("Hello world!");

builder.startTable();
builder.insertCell();
builder.write("Cell 1");
builder.insertCell();
builder.write("Cell 2");
builder.endTable();

builder.insertImage(base.imageDir + "Logo.jpg");            

// Our document contains three Run nodes.
var nodeList = doc.selectNodes("//Run").toArray();

expect(nodeList.length).toEqual(3);
expect(nodeList.find(n => n.getText().trim() == "Hello world!")).not.toEqual(null);
expect(nodeList.find(n => n.getText().trim() == "Cell 1")).not.toEqual(null);
expect(nodeList.find(n => n.getText().trim() == "Cell 2")).not.toEqual(null);

// Use a double forward slash to select all Run nodes
// that are indirect descendants of a Table node, which would be the runs inside the two cells we inserted.
nodeList = doc.selectNodes("//Table//Run").toArray();

expect(nodeList.length).toEqual(2);
expect(nodeList.find(n => n.getText().trim() == "Cell 1")).not.toEqual(null);
expect(nodeList.find(n => n.getText().trim() == "Cell 2")).not.toEqual(null);

// Access the shape that contains the image we inserted.
nodeList = doc.selectNodes("//Shape").toArray();

expect(nodeList.length).toEqual(1);

let shape = nodeList.at(0).asShape();
expect(shape.hasImage).toEqual(true);
```

### See Also

* module [Aspose.Words](../../)
* class [NodeList](../)

