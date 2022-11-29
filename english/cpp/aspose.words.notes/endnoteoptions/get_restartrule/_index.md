---
title: get_RestartRule
second_title: Aspose.Words for C++ API Reference
description: Determines when automatic numbering restarts.
type: docs
weight: 27
url: /cpp/aspose.words.notes/endnoteoptions/get_restartrule/
---
## EndnoteOptions::get_RestartRule method


Determines when automatic numbering restarts.

```cpp
Aspose::Words::Notes::FootnoteNumberingRule Aspose::Words::Notes::EndnoteOptions::get_RestartRule() override
```

## Remarks


Not all values are applicable to endnotes. To ascertain which values are applicable see [FootnoteNumberingRule](../../footnotenumberingrule/).

## Examples



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

## See Also

* Enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words](../../../)
