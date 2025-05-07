---
title: Footnote.footnoteType property
linktitle: footnoteType property
articleTitle: footnoteType property
second_title: Aspose.Words for Node.js
description: "Footnote.footnoteType property. Returns a value that specifies whether this is a footnote or endnote."
type: docs
weight: 30
url: /nodejs-net/aspose.words.notes/footnote/footnoteType/
---

## Footnote.footnoteType property

Returns a value that specifies whether this is a footnote or endnote.


```js
get footnoteType(): Aspose.Words.Notes.FootnoteType
```

### Examples

Shows the difference between footnotes and endnotes.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are two ways of attaching numbered references to the text. Both these references will add a
// small superscript reference mark at the location that we insert them.
// The reference mark, by default, is the index number of the reference among all the references in the document.
// Each reference will also create an entry, which will have the same reference mark as in the body text
// and reference text, which we will pass to the document builder's "InsertFootnote" method.
// 1 -  A footnote, whose entry will appear on the same page as the text that it references:
builder.write("Footnote referenced main body text.");
let footnote = builder.insertFootnote(aw.Notes.FootnoteType.Footnote, 
  "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  An endnote, whose entry will appear at the end of the document:
builder.write("Endnote referenced main body text.");
let endnote = builder.insertFootnote(aw.Notes.FootnoteType.Endnote, 
  "Endnote text, will appear at the very end of the document.");

builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.insertBreak(aw.BreakType.SectionBreakNewPage);

expect(footnote.footnoteType).toEqual(aw.Notes.FootnoteType.Footnote);
expect(endnote.footnoteType).toEqual(aw.Notes.FootnoteType.Endnote);

doc.save(base.artifactsDir + "InlineStory.FootnoteEndnote.docx");
```

### See Also

* module [Aspose.Words.Notes](../../)
* class [Footnote](../)

