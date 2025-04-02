---
title: ListLevelCollection class
linktitle: ListLevelCollection class
articleTitle: ListLevelCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Lists.ListLevelCollection class. A collection of list formatting for each level in a list"
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Lists/listlevelcollection/
---

## ListLevelCollection class

A collection of list formatting for each level in a list.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/nodejs-net/working-with-lists/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of levels in this list. |
| [this[]](./this[]/) |  |

### Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```js
let doc = new aw.Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize the first two of its list levels.
let list = doc.lists.add(aw.Lists.ListTemplate.NumberDefault);

let listLevel = list.listLevels.at(0);
listLevel.font.color = "#FF0000";
listLevel.font.size = 24;
listLevel.numberStyle = aw.NumberStyle.OrdinalText;
listLevel.startAt = 21;
listLevel.numberFormat = "\u0000";

listLevel.numberPosition = -36;
listLevel.textPosition = 144;
listLevel.tabPosition = 144;

listLevel = list.listLevels.at(1);
listLevel.alignment = aw.Lists.ListLevelAlignment.Right;
listLevel.numberStyle = aw.NumberStyle.Bullet;
listLevel.font.name = "Wingdings";
listLevel.font.color = "#0000FF";
listLevel.font.size = 24;

// This NumberFormat value will create star-shaped bullet list symbols.
listLevel.numberFormat = "\uf0af";
listLevel.trailingCharacter = aw.Lists.ListTrailingCharacter.Space;
listLevel.numberPosition = 144;

// Create paragraphs and apply both list levels of our custom list formatting to them.
let builder = new aw.DocumentBuilder(doc);

builder.listFormat.list = list;
builder.writeln("The quick brown fox...");
builder.writeln("The quick brown fox...");

builder.listFormat.listIndent();
builder.writeln("jumped over the lazy dog.");
builder.writeln("jumped over the lazy dog.");

builder.listFormat.listOutdent();
builder.writeln("The quick brown fox...");

builder.listFormat.removeNumbers();

builder.document.save(base.artifactsDir + "Lists.CreateCustomList.docx");
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

### See Also

* module [Aspose.Words.Lists](../)

