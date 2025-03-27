---
title: ListLevel.isLegal property
linktitle: isLegal property
articleTitle: isLegal property
second_title: Aspose.Words for NodeJs
description: "ListLevel.isLegal property. True if the level turns all inherited numbers to Arabic, false if it preserves their number style."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Lists/listlevel/isLegal/
---

## ListLevel.isLegal property

True if the level turns all inherited numbers to Arabic, false if it preserves their number style.


```js
get isLegal(): boolean
```

### Examples

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

