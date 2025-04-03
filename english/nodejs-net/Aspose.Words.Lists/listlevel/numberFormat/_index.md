---
title: ListLevel.numberFormat property
linktitle: numberFormat property
articleTitle: numberFormat property
second_title: Aspose.Words for NodeJs
description: "ListLevel.numberFormat property. Returns or sets the number format for the list level."
type: docs
weight: 70
url: /nodejs-net/aspose.words.lists/listlevel/numberFormat/
---

## ListLevel.numberFormat property

Returns or sets the number format for the list level.


```js
get numberFormat(): string
```

### Remarks

Among normal text characters, the string can contain placeholder characters \\x0000 to \\x0008
representing the numbers from the corresponding list levels.

For example, the string "\\x0000.\\x0001)" will generate a list label
that looks something like "1.5)". The number "1" is the current number from
the 1st list level, the number "5" is the current number from the 2nd list level.

Null is not allowed, but an empty string meaning no number is valid.




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

Shows advances ways of customizing list labels.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
let list = doc.lists.add(aw.Lists.ListTemplate.NumberDefault);

// Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
// These will look like "Appendix A", "Appendix B"...
list.listLevels.at(0).numberFormat = "Appendix \u0000";
list.listLevels.at(0).numberStyle = aw.NumberStyle.UppercaseLetter;
list.listLevels.at(0).linkedStyle = doc.styles.at("Heading 1");

// Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
// If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
list.listLevels.at(1).numberFormat = "Section (\u0000.\u0001)";
list.listLevels.at(1).numberStyle = aw.NumberStyle.LeadingZero;

// Note that the higher-level uses UppercaseLetter numbering.
// We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
list.listLevels.at(1).isLegal = true;
list.listLevels.at(1).restartAfterLevel = 0;

// Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
// These list labels will look like "-I-", "-II-"...
list.listLevels.at(2).numberFormat = "-\u0002-";
list.listLevels.at(2).numberStyle = aw.NumberStyle.UppercaseRoman;
list.listLevels.at(2).restartAfterLevel = 1;

// Make labels of all list levels bold.
for (let level of list.listLevels)
  level.font.bold = true;

// Apply list formatting to the current paragraph.
builder.listFormat.list = list;

// Create list items that will display all three of our list levels.
for (let n = 0; n < 2; n++)
{
  for (let i = 0; i < 3; i++)
  {
    builder.listFormat.listLevelNumber = i;
    builder.writeln("Level " + i);
  }
}

builder.listFormat.removeNumbers();

doc.save(base.artifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### See Also

* module [Aspose.Words.Lists](../../)
* class [ListLevel](../)

