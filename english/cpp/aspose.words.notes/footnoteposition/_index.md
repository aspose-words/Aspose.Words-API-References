---
title: FootnotePosition
second_title: Aspose.Words for C++ API Reference
description: Defines the footnote position.
type: docs
weight: 66
url: /cpp/aspose.words.notes/footnoteposition/
---
## FootnotePosition enum


Defines the footnote position.

### Values

| Name | Value | Description |
| --- | --- | --- |
| BottomOfPage | 1 | Footnotes are output at the bottom of each page. |
| BeneathText | 2 | Footnotes are output beneath text on each page. |


## Examples




Shows how to select a different place where the document collects and displays its footnotes. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A footnote is a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.
// Inserting a footnote adds a small superscript reference symbol
// at the main body text where we insert the footnote.
// Each footnote also creates an entry at the bottom of the page, consisting of a symbol
// that matches the reference symbol in the main body text.
// The reference text that we pass to the document builder's "InsertFootnote" method.
builder->Write(u"Hello world!");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote contents.");

// We can use the "Position" property to determine where the document will place all its footnotes.
// If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
// every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
// If we set the value of the "Position" property to "FootnotePosition.BeneathText",
// every footnote will show up at the end of the page's text that contains its reference mark.
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(ArtifactsDir + u"InlineStory.PositionFootnote.docx");
```

