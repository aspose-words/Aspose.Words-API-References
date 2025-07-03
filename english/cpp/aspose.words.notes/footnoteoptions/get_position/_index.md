---
title: Aspose::Words::Notes::FootnoteOptions::get_Position method
linktitle: get_Position
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::FootnoteOptions::get_Position method. Specifies the footnotes position in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.notes/footnoteoptions/get_position/
---
## FootnoteOptions::get_Position method


Specifies the footnotes position.

```cpp
Aspose::Words::Notes::FootnotePosition Aspose::Words::Notes::FootnoteOptions::get_Position()
```


## Examples



Shows how to select a different place where the document collects and displays its footnotes. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A footnote is a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.
// Inserting a footnote adds a small superscript reference symbol
// at the main body text where we insert the footnote.
// Each footnote also creates an entry at the bottom of the page, consisting of a symbol
// that matches the reference symbol in the main body text.
// The reference text that we pass to the document builder's "InsertFootnote" method.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// We can use the "Position" property to determine where the document will place all its footnotes.
// If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
// every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
// If we set the value of the "Position" property to "FootnotePosition.BeneathText",
// every footnote will show up at the end of the page's text that contains its reference mark.
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```

## See Also

* Enum [FootnotePosition](../../footnoteposition/)
* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
