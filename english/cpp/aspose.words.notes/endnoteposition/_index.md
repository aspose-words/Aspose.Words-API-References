---
title: Aspose::Words::Notes::EndnotePosition enum
linktitle: EndnotePosition
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::EndnotePosition enum. Defines the endnote position in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.notes/endnoteposition/
---
## EndnotePosition enum


Defines the endnote position.

```cpp
enum class EndnotePosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| EndOfSection | 0 | Endnotes are output at the end of the section. |
| EndOfDocument | 3 | Endnotes are output at the end of the document. |


## Examples



Shows how to select a different place where the document collects and displays its endnotes. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// An endnote is a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.
// Inserting an endnote adds a small superscript reference symbol
// at the main body text where we insert the endnote.
// Each endnote also creates an entry at the end of the document, consisting of a symbol
// that matches the reference symbol in the main body text.
// The reference text that we pass to the document builder's "InsertEndnote" method.
builder->Write(u"Hello world!");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// We can use the "Position" property to determine where the document will place all its endnotes.
// If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
// every footnote will show up in a collection at the end of the document. This is the default value.
// If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
// every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(ArtifactsDir + u"InlineStory.PositionEndnote.docx");
```

## See Also

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
