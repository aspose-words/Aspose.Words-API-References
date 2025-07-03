---
title: Aspose::Words::Document::get_EndnoteOptions method
linktitle: get_EndnoteOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_EndnoteOptions method. Provides options that control numbering and positioning of endnotes in this document in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words/document/get_endnoteoptions/
---
## Document::get_EndnoteOptions method


Provides options that control numbering and positioning of endnotes in this document.

```cpp
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> Aspose::Words::Document::get_EndnoteOptions()
```


## Examples



Shows how to select a different place where the document collects and displays its endnotes. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// An endnote is a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.
// Inserting an endnote adds a small superscript reference symbol
// at the main body text where we insert the endnote.
// Each endnote also creates an entry at the end of the document, consisting of a symbol
// that matches the reference symbol in the main body text.
// The reference text that we pass to the document builder's "InsertEndnote" method.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// We can use the "Position" property to determine where the document will place all its endnotes.
// If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
// every footnote will show up in a collection at the end of the document. This is the default value.
// If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
// every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionEndnote.docx");
```


Shows how to change the number style of footnote/endnote reference marks. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Footnotes and endnotes are a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.
// Inserting a footnote/endnote adds a small superscript reference symbol
// at the main body text where we insert the footnote/endnote.
// Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
// symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
// Footnote entries, by default, show up at the bottom of each page that contains
// their reference symbols, and endnotes show up at the end of the document.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// By default, the reference symbol for each footnote and endnote is its index
// among all the document's footnotes/endnotes. Each document maintains separate counts
// for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
// and endnotes display their numbers in lowercase Roman numerals.
ASSERT_EQ(Aspose::Words::NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(Aspose::Words::NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
// This will not affect footnotes/endnotes with custom reference marks.
doc->get_FootnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);

doc->Save(get_ArtifactsDir() + u"InlineStory.RefMarkNumberStyle.docx");
```


Shows how to restart footnote/endnote numbering at certain places in the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Footnotes and endnotes are a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.
// Inserting a footnote/endnote adds a small superscript reference symbol
// at the main body text where we insert the footnote/endnote.
// Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
// symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
// Footnote entries, by default, show up at the bottom of each page that contains
// their reference symbols, and endnotes show up at the end of the document.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 4.");

// By default, the reference symbol for each footnote and endnote is its index
// among all the document's footnotes/endnotes. Each document maintains separate counts
// for footnotes and endnotes and does not restart these counts at any point.
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), Aspose::Words::Notes::FootnoteNumberingRule::Default);
ASSERT_EQ(Aspose::Words::Notes::FootnoteNumberingRule::Default, Aspose::Words::Notes::FootnoteNumberingRule::Continuous);

// We can use the "RestartRule" property to get the document to restart
// the footnote/endnote counts at a new page or section.
doc->get_FootnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartSection);

doc->Save(get_ArtifactsDir() + u"InlineStory.NumberingRule.docx");
```


Shows how to set a number at which the document begins the footnote/endnote count. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Footnotes and endnotes are a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.
// Inserting a footnote/endnote adds a small superscript reference symbol
// at the main body text where we insert the footnote/endnote.
// Each footnote/endnote also creates an entry, which consists of a symbol
// that matches the reference symbol in the main body text.
// The reference text that we pass to the document builder's "InsertEndnote" method.
// Footnote entries, by default, show up at the bottom of each page that contains
// their reference symbols, and endnotes show up at the end of the document.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");

// By default, the reference symbol for each footnote and endnote is its index
// among all the document's footnotes/endnotes. Each document maintains separate counts
// for footnotes and for endnotes, which both begin at 1.
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// We can use the "StartNumber" property to get the document to
// begin a footnote or endnote count at a different number.
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(get_ArtifactsDir() + u"InlineStory.StartNumber.docx");
```

## See Also

* Class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
