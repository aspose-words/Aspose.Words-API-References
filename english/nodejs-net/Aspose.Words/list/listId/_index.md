---
title: List.listId property
linktitle: listId property
articleTitle: listId property
second_title: Aspose.Words for NodeJs
description: "List.listId property. Gets the unique identifier of the list."
type: docs
weight: 60
url: /nodejs-net/aspose.words/list/listId/
---

## List.listId property

Gets the unique identifier of the list.


```js
get listId(): number
```

### Remarks

You do not normally need to use this property. But if you use it, you normally do so
in conjunction with the [ListCollection.getListByListId()](../../../aspose.words.lists/listcollection/getListByListId/#number) method to find a
list by its identifier.




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

Shows how to verify owner document properties of lists.

```js
let doc = new aw.Document();

let lists = doc.lists;
expect(lists.document.referenceEquals(doc)).toEqual(true);

let list = lists.add(aw.Lists.ListTemplate.BulletDefault);
expect(list.document.referenceEquals(doc)).toBe(true);

console.log("Current list count: " + lists.count);
console.log("Is the first document list: " + (lists.at(0).equals(list)));
console.log("ListId: " + list.listId);
console.log("List is the same by ListId: " + (lists.getListByListId(1).equals(list)));
```

### See Also

* module [Aspose.Words](../../)
* class [List](../)

