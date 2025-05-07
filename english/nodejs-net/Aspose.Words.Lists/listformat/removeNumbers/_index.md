---
title: ListFormat.removeNumbers method
linktitle: removeNumbers method
articleTitle: removeNumbers method
second_title: Aspose.Words for Node.js
description: "ListFormat.removeNumbers method. Removes numbers or bullets from the current paragraph and sets list level to zero."
type: docs
weight: 90
url: /nodejs-net/aspose.words.lists/listformat/removeNumbers/
---

## removeNumbers() {#default}

Removes numbers or bullets from the current paragraph and sets list level to zero.


```js
removeNumbers()
```

### Remarks

Calling this method is equivalent to setting the [ListFormat.list](../list/) property to ``null``.




### Examples

Shows how to create bulleted and numbered lists.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Aspose.words main advantages are:");

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create with a document builder.
// 1 -  A bulleted list:
// This list will apply an indent and a bullet symbol ("•") before each paragraph.
builder.listFormat.applyBulletDefault();
builder.writeln("Great performance");
builder.writeln("High reliability");
builder.writeln("Quality code and working");
builder.writeln("Wide variety of features");
builder.writeln("Easy to understand API");

// End the bulleted list.
builder.listFormat.removeNumbers();

builder.insertBreak(aw.BreakType.ParagraphBreak);
builder.writeln("Aspose.words allows:");

// 2 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder.listFormat.applyNumberDefault();

// This paragraph is the first item. The first item of a numbered list will have a "1." as its list item symbol.
builder.writeln("Opening documents from different formats:");

expect(builder.listFormat.listLevelNumber).toEqual(0);

// Call the "ListIndent" method to increase the current list level,
// which will start a new self-contained list, with a deeper indent, at the current item of the first list level.
builder.listFormat.listIndent();

expect(builder.listFormat.listLevelNumber).toEqual(1);

// These are the first three list items of the second list level, which will maintain a count
// independent of the count of the first list level. According to the current list format,
// they will have symbols of "a.", "b.", and "c.".
builder.writeln("DOC");
builder.writeln("PDF");
builder.writeln("HTML");

// Call the "ListOutdent" method to return to the previous list level.
builder.listFormat.listOutdent();

expect(builder.listFormat.listLevelNumber).toEqual(0);

// These two paragraphs will continue the count of the first list level.
// These items will have symbols of "2.", and "3."
builder.writeln("Processing documents");
builder.writeln("Saving documents in different formats:");

// If we increase the list level to a level that we have added items to previously,
// the nested list will be separate from the previous, and its numbering will start from the beginning. 
// These list items will have symbols of "a.", "b.", "c.", "d.", and "e".
builder.listFormat.listIndent();
builder.writeln("DOC");
builder.writeln("PDF");
builder.writeln("HTML");
builder.writeln("MHTML");
builder.writeln("Plain text");

// Outdent the list level again.
builder.listFormat.listOutdent();
builder.writeln("Doing many other things!");

// End the numbered list.
builder.listFormat.removeNumbers();

doc.save(base.artifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

Shows how to remove list formatting from all paragraphs in the main text of a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.listFormat.applyNumberDefault();
builder.writeln("Numbered list item 1");
builder.writeln("Numbered list item 2");
builder.writeln("Numbered list item 3");
builder.listFormat.removeNumbers();

let paras = doc.getChildNodes(aw.NodeType.Paragraph, true).toArray();
expect(paras.filter(n => n.asParagraph().listFormat.isListItem).length).toEqual(3);

for (let n of paras)
  n.asParagraph().listFormat.removeNumbers();

expect(paras.filter(n => n.asParagraph().listFormat.isListItem).length).toEqual(0);
```

### See Also

* module [Aspose.Words.Lists](../../)
* class [ListFormat](../)

