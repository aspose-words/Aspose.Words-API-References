---
title: Aspose::Words::Notes::Footnote::get_FootnoteType method
linktitle: get_FootnoteType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::Footnote::get_FootnoteType method. Returns a value that specifies whether this is a footnote or endnote in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.notes/footnote/get_footnotetype/
---
## Footnote::get_FootnoteType method


Returns a value that specifies whether this is a footnote or endnote.

```cpp
Aspose::Words::Notes::FootnoteType Aspose::Words::Notes::Footnote::get_FootnoteType() const
```


## Examples



Shows the difference between footnotes and endnotes. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Below are two ways of attaching numbered references to the text. Both these references will add a
// small superscript reference mark at the location that we insert them.
// The reference mark, by default, is the index number of the reference among all the references in the document.
// Each reference will also create an entry, which will have the same reference mark as in the body text
// and reference text, which we will pass to the document builder's "InsertFootnote" method.
// 1 -  A footnote, whose entry will appear on the same page as the text that it references:
builder->Write(u"Footnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  An endnote, whose entry will appear at the end of the document:
builder->Write(u"Endnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> endnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote text, will appear at the very end of the document.");

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Footnote, footnote->get_FootnoteType());
ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Endnote, endnote->get_FootnoteType());

doc->Save(get_ArtifactsDir() + u"InlineStory.FootnoteEndnote.docx");
```

## See Also

* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
