---
title: ListCollection class
linktitle: ListCollection class
articleTitle: ListCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Lists.ListCollection class. Stores and manages formatting of bulleted and numbered lists used in a document"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Lists/listcollection/
---

## ListCollection class

Stores and manages formatting of bulleted and numbered lists used in a document.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/nodejs-net/working-with-lists/) documentation article.




### Remarks

A list in a Microsoft Word document is a set of list formatting properties.
The formatting of the lists is stored in the [ListCollection](./) collection separately
from the paragraphs of text.

You do not create objects of this class. There is always only one [ListCollection](./)
object per document and it is accessible via the [DocumentBase.lists](../../Aspose.Words/documentbase/lists/) property.

To create a new list based on a predefined list template or based on a list style,
use the [ListCollection.add()](./add/#style) method.

To create a new list with formatting identical to an existing list,
use the [ListCollection.addCopy()](./addCopy/#list) method.

To make a paragraph bulleted or numbered, you need to apply list formatting
to a paragraph by assigning a [List](../../Aspose.Words/list/) object to the
[ListFormat.list](../listformat/list/) property of [ListFormat](../listformat/).

To remove list formatting from a paragraph, use the [ListFormat.removeNumbers()](../listformat/removeNumbers/#default)
method.

If you know a bit about WordprocessingML, then you might know it defines separate concepts
for "list" and "list definition". This exactly corresponds to how list formatting is stored
in a Microsoft Word document at the low level. List definition is like a "schema" and
list is like an instance of a list definition.

To simplify programming model, Aspose.Words hides the distinction between list and list
definition in much the same way like Microsoft Word hides this in its user interface.
This allows you to concentrate more on how you want your document to look like, rather than
building low-level objects to satisfy requirements of the Microsoft Word file format.

It is not possible to delete lists once they are created in the current version of Aspose.Words.
This is similar to Microsoft Word where user does not have explicit control over list definitions.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the count of numbered and bulleted lists in the document. |
| [document](./document/) | Gets the owner document. |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ add(listTemplate)](./add/#listtemplate) | Creates a new list based on a predefined template and adds it to the collection of lists in the document. |
|[ add(listStyle)](./add/#style) | Creates a new list that references a list style and adds it to the collection of lists in the document. |
|[ addCopy(srcList)](./addCopy/#list) | Creates a new list by copying the specified list and adding it to the collection of lists in the document. |
|[ addSingleLevelList(listTemplate)](./addSingleLevelList/#listtemplate) | Creates a new single level list based on the predefined template and adds it to the list collection in the document. |
|[ getListByListId(listId)](./getListByListId/#number) | Gets a list by a list identifier. |

### Examples

Shows how to work with list levels.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

expect(builder.listFormat.isListItem).toEqual(false);

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create using a document builder.
// 1 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder.listFormat.list = doc.lists.add(aw.Lists.ListTemplate.NumberDefault);

expect(builder.listFormat.isListItem).toEqual(true);

// By setting the "ListLevelNumber" property, we can increase the list level
// to begin a self-contained sub-list at the current list item.
// The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
// Deeper list levels use letters and lowercase Roman numerals. 
for (let i = 0; i < 9; i++)
{
  builder.listFormat.listLevelNumber = i;
  builder.writeln("Level " + i);
}

// 2 -  A bulleted list:
// This list will apply an indent and a bullet symbol ("•") before each paragraph.
// Deeper levels of this list will use different symbols, such as "■" and "○".
builder.listFormat.list = doc.lists.add(aw.Lists.ListTemplate.BulletDefault);

for (let i = 0; i < 9; i++)
{
  builder.listFormat.listLevelNumber = i;
  builder.writeln("Level " + i);
}

// We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
builder.listFormat.list = null;

expect(builder.listFormat.isListItem).toEqual(false);

doc.save(base.artifactsDir + "Lists.SpecifyListLevel.docx");
```

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

* module [Aspose.Words.Lists](../)
* class [List](../../Aspose.Words/list/)
* class [ListLevel](../listlevel/)
* class [ListFormat](../listformat/)

