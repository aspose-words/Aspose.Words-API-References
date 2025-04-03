---
title: ListCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Lists.ListCollection.add method"
type: docs
weight: 40
url: /nodejs-net/aspose.words.lists/listcollection/add/
---

## add(listTemplate) {#listtemplate}

Creates a new list based on a predefined template and adds it to the collection of lists in the document.


```js
add(listTemplate: Aspose.Words.Lists.ListTemplate)
```

| Parameter | Type | Description |
| --- | --- | --- |
| listTemplate | [ListTemplate](../../listtemplate/) | The template of the list. |

### Remarks

Aspose.Words list templates correspond to the 21 list templates available
in the Bullets and Numbering dialog box in Microsoft Word 2003.

All lists created using this method have 9 list levels.




### Returns

The newly created list.


## add(listStyle) {#style}

Creates a new list that references a list style and adds it to the collection of lists in the document.


```js
add(listStyle: Aspose.Words.Style)
```

| Parameter | Type | Description |
| --- | --- | --- |
| listStyle | [Style](../../../aspose.words/style/) | The list style. |

### Remarks

The newly created list references the list style. If you change the properties of the list
style, it is reflected in the properties of the list. Vice versa, if you change the properties
of the list, it is reflected in the properties of the list style.




### Returns

The newly created list.


## Examples

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

Shows how to create a list by applying a new list format to a collection of paragraphs.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Paragraph 1");
builder.writeln("Paragraph 2");
builder.write("Paragraph 3");

let paras = doc.getChildNodes(aw.NodeType.Paragraph, true).toArray();

expect(paras.filter(n => n.asParagraph().listFormat.isListItem).length).toEqual(0);

let list = doc.lists.add(aw.Lists.ListTemplate.NumberUppercaseLetterDot);

for (let node of paras)
{
  let paragraph = node.asParagraph();
  paragraph.listFormat.list = list;
  paragraph.listFormat.listLevelNumber = 1;
}

expect(paras.filter(n => n.asParagraph().listFormat.isListItem).length).toEqual(3);
```

Shows how to create a list style and use it in a document.

```js
let doc = new aw.Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// We can contain an entire List object within a style.
let listStyle = doc.styles.add(aw.StyleType.List, "MyListStyle");

let list1 = listStyle.list;

expect(list1.isListStyleDefinition).toEqual(true);
expect(list1.isListStyleReference).toEqual(false);
expect(list1.isMultiLevel).toEqual(true);
expect(list1.style).toEqual(listStyle);

// Change the appearance of all list levels in our list.
for (let level of list1.listLevels)
{
  level.font.name = "Verdana";
  level.font.color = "#0000FF";
  level.font.bold = true;
}

let builder = new aw.DocumentBuilder(doc);

builder.writeln("Using list style first time:");

// Create another list from a list within a style.
let list2 = doc.lists.add(listStyle);

expect(list2.isListStyleDefinition).toEqual(false);
expect(list2.isListStyleReference).toEqual(true);
expect(list2.style).toEqual(listStyle);

// Add some list items that our list will format.
builder.listFormat.list = list2;
builder.writeln("Item 1");
builder.writeln("Item 2");
builder.listFormat.removeNumbers();

builder.writeln("Using list style second time:");

// Create and apply another list based on the list style.
let list3 = doc.lists.add(listStyle);
builder.listFormat.list = list3;
builder.writeln("Item 1");
builder.writeln("Item 2");
builder.listFormat.removeNumbers();

builder.document.save(base.artifactsDir + "Lists.CreateAndUseListStyle.docx");
```

## See Also

* module [Aspose.Words.Lists](../../)
* class [ListCollection](../)

