---
title: FootnotePosition enumeration
linktitle: FootnotePosition enumeration
articleTitle: FootnotePosition enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Notes.FootnotePosition enumeration. Defines the footnote position."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Notes/footnoteposition/
---

## FootnotePosition enumeration

Defines the footnote position.


### Members

| Name | Description |
| --- | --- |
| BottomOfPage | Footnotes are output at the bottom of each page. |
| BeneathText | Footnotes are output beneath text on each page. |

### Examples

Shows how to select a different place where the document collects and displays its footnotes.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// A footnote is a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.  
// Inserting a footnote adds a small superscript reference symbol
// at the main body text where we insert the footnote.
// Each footnote also creates an entry at the bottom of the page, consisting of a symbol
// that matches the reference symbol in the main body text.
// The reference text that we pass to the document builder's "InsertFootnote" method.
builder.write("Hello world!");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote contents.");

// We can use the "Position" property to determine where the document will place all its footnotes.
// If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
// every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
// If we set the value of the "Position" property to "FootnotePosition.BeneathText",
// every footnote will show up at the end of the page's text that contains its reference mark.
doc.footnoteOptions.position = footnotePosition;

doc.save(base.artifactsDir + "InlineStory.PositionFootnote.docx");
```

### See Also

* module [Aspose.Words.Notes](../)
* class [FootnoteOptions](../footnoteoptions/)

