---
title: ListFormat.list property
linktitle: list property
articleTitle: list property
second_title: Aspose.Words for NodeJs
description: "ListFormat.list property. Gets or sets the list this paragraph is a member of."
type: docs
weight: 20
url: /nodejs-net/aspose.words.lists/listformat/list/
---

## ListFormat.list property

Gets or sets the list this paragraph is a member of.


```js
get list(): Aspose.Words.Lists.List
```

### Remarks

The list that is being assigned to this property must belong to the current document.

The list that is being assigned to this property must not be a list style definition.

Setting this property to ``null`` removes bullets and numbering from the paragraph
and sets the list level number to zero. Setting this property to ``null`` is equivalent
to calling [ListFormat.removeNumbers()](../removeNumbers/#default).




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

Shows how to nest a list inside another list.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create an outline list for the headings.
let outlineList = doc.lists.add(aw.Lists.ListTemplate.OutlineNumbers);
builder.listFormat.list = outlineList;
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;
builder.writeln("This is my Chapter 1");

// Create a numbered list.
let numberedList = doc.lists.add(aw.Lists.ListTemplate.NumberDefault);
builder.listFormat.list = numberedList;
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Normal;
builder.writeln("Numbered list item 1.");

// Every paragraph that comprises a list will have this flag.
expect(builder.currentParagraph.isListItem).toEqual(true);
expect(builder.paragraphFormat.isListItem).toEqual(true);

// Create a bulleted list.
let bulletedList = doc.lists.add(aw.Lists.ListTemplate.BulletDefault);
builder.listFormat.list = bulletedList;
builder.paragraphFormat.leftIndent = 72;
builder.writeln("Bulleted list item 1.");
builder.writeln("Bulleted list item 2.");
builder.paragraphFormat.clearFormatting();

// Revert to the numbered list.
builder.listFormat.list = numberedList;
builder.writeln("Numbered list item 2.");
builder.writeln("Numbered list item 3.");

// Revert to the outline list.
builder.listFormat.list = outlineList;
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;
builder.writeln("This is my Chapter 2");

builder.paragraphFormat.clearFormatting();

builder.document.save(base.artifactsDir + "Lists.NestedLists.docx");
```

### See Also

* module [Aspose.Words.Lists](../../)
* class [ListFormat](../)
* property [ListFormat.listLevelNumber](../listLevelNumber/)
* method [ListFormat.removeNumbers()](../removeNumbers/#default)

