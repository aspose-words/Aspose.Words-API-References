---
title: List class
linktitle: List class
articleTitle: List class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.List class. Represents formatting of a list"
type: docs
weight: 780
url: /nodejs-net/Aspose.Words/list/
---

## List class

Represents formatting of a list.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/nodejs-net/working-with-lists/) documentation article.




### Remarks

A list in a Microsoft Word document is a set of list formatting properties.
Each list can have up to 9 levels and formatting properties, such as number style, start value,
indent, tab position etc are defined separately for each level.

A [List](./) object always belongs to the [ListCollection](../../Aspose.Words.Lists/listcollection/) collection.

To create a new list, use the Add methods of the [ListCollection](../../Aspose.Words.Lists/listcollection/) collection.

To modify formatting of a list, use [ListLevel](../../Aspose.Words.Lists/listlevel/) objects found in
the [List.listLevels](./listLevels/) collection.

To apply or remove list formatting from a paragraph, use [ListFormat](../../Aspose.Words.Lists/listformat/).




### Properties

| Name | Description |
| --- | --- |
| [document](./document/) | Gets the owner document. |
| [isListStyleDefinition](./isListStyleDefinition/) | Returns ``True`` if this list is a definition of a list style. |
| [isListStyleReference](./isListStyleReference/) | Returns ``True`` if this list is a reference to a list style. |
| [isMultiLevel](./isMultiLevel/) | Returns ``True`` when the list contains 9 levels; ``False`` when 1 level. |
| [isRestartAtEachSection](./isRestartAtEachSection/) | Specifies whether list should be restarted at each section. Default value is ``False``. |
| [listId](./listId/) | Gets the unique identifier of the list. |
| [listLevels](./listLevels/) | Gets the collection of list levels for this list. |
| [style](./style/) | Gets the list style that this list references or defines. |

### Methods

| Name | Description |
| --- | --- |
|[ compareTo(obj)](./compareTo/#object) | Compares the specified object to the current object. |
|[ compareTo(other)](./compareTo/#list) | Compares the specified list to the current list. |
|[ equals(list)](./equals/#list) | Compares with the specified list. |
|[ hasSameTemplate(other)](./hasSameTemplate/#list) | Returns true if the current list and the given list are created from the same template. |

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

### See Also

* module [Aspose.Words](../)
* class [ListCollection](../../Aspose.Words.Lists/listcollection/)
* class [ListLevel](../../Aspose.Words.Lists/listlevel/)
* class [ListFormat](../../Aspose.Words.Lists/listformat/)

