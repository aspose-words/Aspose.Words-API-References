---
title: Aspose::Words::Notes::FootnoteOptions class
linktitle: FootnoteOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::FootnoteOptions class. Represents the footnote numbering options for a document or section. To learn more, visit the  documentation article in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.notes/footnoteoptions/
---
## FootnoteOptions class


Represents the footnote numbering options for a document or section. To learn more, visit the [Working with Footnote and Endnote](https://docs.aspose.com/words/cpp/working-with-footnote-and-endnote/) documentation article.

```cpp
class FootnoteOptions : public Aspose::Words::Notes::IFootnoteOptions
```

## Methods

| Method | Description |
| --- | --- |
| [get_Columns](./get_columns/)() | Specifies the number of columns with which the footnotes area is formatted. |
| [get_NumberStyle](./get_numberstyle/)() override | Specifies the number format for automatically numbered footnotes. |
| [get_Position](./get_position/)() | Specifies the footnotes position. |
| [get_RestartRule](./get_restartrule/)() override | Determines when automatic numbering restarts. |
| [get_StartNumber](./get_startnumber/)() override | Specifies the starting number or character for the first automatically numbered footnotes. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Columns](./set_columns/)(int32_t) | Setter for [Aspose::Words::Notes::FootnoteOptions::get_Columns](./get_columns/). |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) override | Setter for [Aspose::Words::Notes::FootnoteOptions::get_NumberStyle](./get_numberstyle/). |
| [set_Position](./set_position/)(Aspose::Words::Notes::FootnotePosition) | Setter for [Aspose::Words::Notes::FootnoteOptions::get_Position](./get_position/). |
| [set_RestartRule](./set_restartrule/)(Aspose::Words::Notes::FootnoteNumberingRule) override | Setter for [Aspose::Words::Notes::FootnoteOptions::get_RestartRule](./get_restartrule/). |
| [set_StartNumber](./set_startnumber/)(int32_t) override | Setter for [Aspose::Words::Notes::FootnoteOptions::get_StartNumber](./get_startnumber/). |
| static [Type](./type/)() |  |

## Examples



Shows how to split the footnote section into a given number of columns. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(ArtifactsDir + u"Document.FootnoteColumns.docx");
```


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


Shows how to change the number style of footnote/endnote reference marks. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Footnotes and endnotes are a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.
// Inserting a footnote/endnote adds a small superscript reference symbol
// at the main body text where we insert the footnote/endnote.
// Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
// symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
// Footnote entries, by default, show up at the bottom of each page that contains
// their reference symbols, and endnotes show up at the end of the document.
builder->Write(u"Text 1. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// By default, the reference symbol for each footnote and endnote is its index
// among all the document's footnotes/endnotes. Each document maintains separate counts
// for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
// and endnotes display their numbers in lowercase Roman numerals.
ASSERT_EQ(NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
// This will not affect footnotes/endnotes with custom reference marks.
doc->get_FootnoteOptions()->set_NumberStyle(NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(NumberStyle::UppercaseLetter);

doc->Save(ArtifactsDir + u"InlineStory.RefMarkNumberStyle.docx");
```


Shows how to restart footnote/endnote numbering at certain places in the document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Footnotes and endnotes are a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow.
// Inserting a footnote/endnote adds a small superscript reference symbol
// at the main body text where we insert the footnote/endnote.
// Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
// symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
// Footnote entries, by default, show up at the bottom of each page that contains
// their reference symbols, and endnotes show up at the end of the document.
builder->Write(u"Text 1. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 2.");
builder->InsertBreak(BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 4.");

// By default, the reference symbol for each footnote and endnote is its index
// among all the document's footnotes/endnotes. Each document maintains separate counts
// for footnotes and endnotes and does not restart these counts at any point.
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), FootnoteNumberingRule::Default);
ASSERT_EQ(FootnoteNumberingRule::Default, FootnoteNumberingRule::Continuous);

// We can use the "RestartRule" property to get the document to restart
// the footnote/endnote counts at a new page or section.
doc->get_FootnoteOptions()->set_RestartRule(FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(FootnoteNumberingRule::RestartSection);

doc->Save(ArtifactsDir + u"InlineStory.NumberingRule.docx");
```


Shows how to set a number at which the document begins the footnote/endnote count. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

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
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(FootnoteType::Endnote, u"Endnote 3.");

// By default, the reference symbol for each footnote and endnote is its index
// among all the document's footnotes/endnotes. Each document maintains separate counts
// for footnotes and for endnotes, which both begin at 1.
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// We can use the "StartNumber" property to get the document to
// begin a footnote or endnote count at a different number.
doc->get_EndnoteOptions()->set_NumberStyle(NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(ArtifactsDir + u"InlineStory.StartNumber.docx");
```

## See Also

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
