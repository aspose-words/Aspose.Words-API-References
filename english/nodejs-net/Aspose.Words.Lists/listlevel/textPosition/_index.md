﻿---
title: ListLevel.textPosition property
linktitle: textPosition property
articleTitle: textPosition property
second_title: Aspose.Words for Node.js
description: "ListLevel.textPosition property. Returns or sets the position (in points) for the second line of wrapping text for the list level."
type: docs
weight: 130
url: /nodejs-net/aspose.words.lists/listlevel/textPosition/
---

## ListLevel.textPosition property

Returns or sets the position (in points) for the second line of wrapping text for the list level.


```js
get textPosition(): number
```

### Remarks

[ListLevel.textPosition](./) corresponds to LeftIndent of the paragraph.




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

* module [Aspose.Words.Lists](../../)
* class [ListLevel](../)
* property [ListLevel.numberPosition](../numberPosition/)
* property [ListLevel.tabPosition](../tabPosition/)

