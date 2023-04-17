---
title: Aspose::Words::Notes::FootnoteNumberingRule enum
linktitle: FootnoteNumberingRule
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::FootnoteNumberingRule enum. Determines when automatic footnote or endnote numbering restarts in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enum


Determines when automatic footnote or endnote numbering restarts.

```cpp
enum class FootnoteNumberingRule
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Continuous | 0 | Numbering continuous throughout the document. |
| RestartSection | 1 | Numbering restarts at each section. |
| RestartPage | 2 | Numbering restarts at each page. Valid for footnotes only. |
| Default | n/a | Equals [Continuous](./). |


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
