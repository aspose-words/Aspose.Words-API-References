---
title: ListLevel class
linktitle: ListLevel class
articleTitle: ListLevel class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Lists.ListLevel class. Defines formatting for a list level"
type: docs
weight: 40
url: /nodejs-net/aspose.words.lists/listlevel/
---

## ListLevel class

Defines formatting for a list level.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/nodejs-net/working-with-lists/) documentation article.




### Remarks

You do not create objects of this class. List level objects are created automatically
when a list is created. You access [ListLevel](./) objects via the
[ListLevelCollection](../listlevelcollection/) collection.

Use the properties of [ListLevel](./) to specify list formatting
for individual list levels.




### Properties

| Name | Description |
| --- | --- |
| [alignment](./alignment/) | Gets or sets the justification of the actual number of the list item. |
| [customNumberStyleFormat](./customNumberStyleFormat/) | Gets or sets the custom number style format for this list level. For example: "a, ç, ĝ, ...". |
| [font](./font/) | Specifies character formatting used for the list label. |
| [imageData](./imageData/) | Returns image data of the picture bullet shape for the current list level. |
| [isLegal](./isLegal/) | True if the level turns all inherited numbers to Arabic, false if it preserves their number style. |
| [linkedStyle](./linkedStyle/) | Gets or sets the paragraph style that is linked to this list level. |
| [numberFormat](./numberFormat/) | Returns or sets the number format for the list level. |
| [numberPosition](./numberPosition/) | Returns or sets the position (in points) of the number or bullet for the list level. |
| [numberStyle](./numberStyle/) | Returns or sets the number style for this list level. |
| [restartAfterLevel](./restartAfterLevel/) | Sets or returns the list level that must appear before the specified list level restarts numbering. |
| [startAt](./startAt/) | Returns or sets the starting number for this list level. |
| [tabPosition](./tabPosition/) | Returns or sets the tab position (in points) for the list level. |
| [textPosition](./textPosition/) | Returns or sets the position (in points) for the second line of wrapping text for the list level. |
| [trailingCharacter](./trailingCharacter/) | Returns or sets the character inserted after the number for the list level. |

### Methods

| Name | Description |
| --- | --- |
|[ createPictureBullet()](./createPictureBullet/#default) | Creates picture bullet shape for the current list level. |
|[ deletePictureBullet()](./deletePictureBullet/#default) | Deletes picture bullet for the current list level. |
|[ equals(level)](./equals/#listlevel) | Compares with the specified ListLevel. |
|[ getEffectiveValue(index, numberStyle, customNumberStyleFormat)](./getEffectiveValue/#number_numberstyle_string) | Reports the string representation of the [ListLevel](./) object for the specified index of the list item. Parameters specify the [NumberStyle](../../aspose.words/numberstyle/) and an optional format string used when [NumberStyle.Custom](../../aspose.words/numberstyle/#Custom) is specified. |

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

### See Also

* module [Aspose.Words.Lists](../)

