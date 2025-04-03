---
title: ListCollection.addCopy method
linktitle: addCopy method
articleTitle: addCopy method
second_title: Aspose.Words for NodeJs
description: "ListCollection.addCopy method. Creates a new list by copying the specified list and adding it to the collection of lists in the document."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Lists/listcollection/addCopy/
---

## addCopy(srcList) {#list}

Creates a new list by copying the specified list and adding it to the collection of lists in the document.


```js
addCopy(srcList: Aspose.Words.Lists.List)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcList | [List](../../../aspose.words/list/) | The source list to copy from. |

### Remarks

The source list can be from any document. If the source list belongs to a different document,
a copy of the list is created and added to the current document.

If the source list is a reference to or a definition of a list style,
the newly created list is not related to the original list style.




### Returns

The newly created list.


### Examples

Shows how to restart numbering in a list by copying a list.

```js
let doc = new aw.Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize its first list level.
let list1 = doc.lists.add(aw.Lists.ListTemplate.NumberArabicParenthesis);
list1.listLevels.at(0).font.color = "#FF0000";
list1.listLevels.at(0).alignment = aw.Lists.ListLevelAlignment.Right;

// Apply our list to some paragraphs.
let builder = new aw.DocumentBuilder(doc);

builder.writeln("List 1 starts below:");
builder.listFormat.list = list1;
builder.writeln("Item 1");
builder.writeln("Item 2");
builder.listFormat.removeNumbers();

// We can add a copy of an existing list to the document's list collection
// to create a similar list without making changes to the original.
let list2 = doc.lists.addCopy(list1);
list2.listLevels.at(0).font.color = "#0000FF";
list2.listLevels.at(0).startAt = 10;

// Apply the second list to new paragraphs.
builder.writeln("List 2 starts below:");
builder.listFormat.list = list2;
builder.writeln("Item 1");
builder.writeln("Item 2");
builder.listFormat.removeNumbers();

doc.save(base.artifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Shows how to create a document with a sample of all the lists from another document.

```js
test('PrintOutAllLists', () => {
  let srcDoc = new aw.Document(base.myDir + "Rendering.docx");

  let dstDoc = new aw.Document();
  let builder = new aw.DocumentBuilder(dstDoc);

  for (let srcList of srcDoc.lists)
  {
    let dstList = dstDoc.lists.addCopy(srcList);
    addListSample(builder, dstList);
  }

  dstDoc.save(base.artifactsDir + "Lists.PrintOutAllLists.docx");
});

function addListSample(builder, list) {
  builder.writeln("Sample formatting of list with ListId:" + list.listId);
  builder.listFormat.list = list;
  for (let i = 0; i < list.listLevels.count; i++)
  {
    builder.listFormat.listLevelNumber = i;
    builder.writeln("Level " + i);
  }

  builder.listFormat.removeNumbers();
  builder.writeln();
}
```

### See Also

* module [Aspose.Words.Lists](../../)
* class [ListCollection](../)

