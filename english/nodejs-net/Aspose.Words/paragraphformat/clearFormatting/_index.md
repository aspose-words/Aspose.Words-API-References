---
title: ParagraphFormat.clearFormatting method
linktitle: clearFormatting method
articleTitle: clearFormatting method
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.clearFormatting method. Resets to default paragraph formatting."
type: docs
weight: 430
url: /nodejs-net/Aspose.Words/paragraphformat/clearFormatting/
---

## clearFormatting() {#default}

Resets to default paragraph formatting.


```js
clearFormatting()
```

### Remarks

Default paragraph formatting is Normal style, left aligned, no indentation,
no spacing, no borders and no shading.


### Examples

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

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

