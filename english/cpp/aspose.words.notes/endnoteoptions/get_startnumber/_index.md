---
title: get_StartNumber
second_title: Aspose.Words for C++ API Reference
description: Specifies the starting number or character for the first automatically numbered endnotes.
type: docs
weight: 40
url: /cpp/aspose.words.notes/endnoteoptions/get_startnumber/
---
## EndnoteOptions::get_StartNumber method


Specifies the starting number or character for the first automatically numbered endnotes.

```cpp
int32_t Aspose::Words::Notes::EndnoteOptions::get_StartNumber() override
```

## Remarks


This property has effect only when [RestartRule](../get_restartrule/) is set to [Continuous](../../footnotenumberingrule/).

## Examples



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

* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words](../../../)
