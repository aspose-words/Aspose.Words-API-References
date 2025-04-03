---
title: EndnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for NodeJs
description: "EndnoteOptions.position property. Specifies the endnotes position."
type: docs
weight: 20
url: /nodejs-net/aspose.words.notes/endnoteoptions/position/
---

## EndnoteOptions.position property

Specifies the endnotes position.


```js
get position(): Aspose.Words.Notes.EndnotePosition
```

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// An endnote is a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow. 
// Inserting an endnote adds a small superscript reference symbol
// at the main body text where we insert the endnote.
// Each endnote also creates an entry at the end of the document, consisting of a symbol
// that matches the reference symbol in the main body text.
// The reference text that we pass to the document builder's "InsertEndnote" method.
builder.write("Hello world!");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote contents.");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.write("This is the second section.");

// We can use the "Position" property to determine where the document will place all its endnotes.
// If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
// every footnote will show up in a collection at the end of the document. This is the default value.
// If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
// every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
doc.endnoteOptions.position = endnotePosition;

doc.save(base.artifactsDir + "InlineStory.PositionEndnote.docx");
```

### See Also

* module [Aspose.Words.Notes](../../)
* class [EndnoteOptions](../)

