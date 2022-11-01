---
title: get_EndnoteOptions
second_title: Aspose.Words for C++ API Reference
description: Provides options that control numbering and positioning of endnotes in this section.
type: docs
weight: 157
url: /cpp/aspose.words/pagesetup/get_endnoteoptions/
---
## PageSetup.get_EndnoteOptions method


Provides options that control numbering and positioning of endnotes in this section.

```cpp
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> Aspose::Words::PageSetup::get_EndnoteOptions()
```


## Examples




Shows how to configure options affecting footnotes/endnotes in a section. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Hello world!");
builder->InsertFootnote(FootnoteType::Footnote, u"Footnote reference text.");

// Configure all footnotes in the first section to restart the numbering from 1
// at each new page and display themselves directly beneath the text on every page.
SharedPtr<FootnoteOptions> footnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_FootnoteOptions();
footnoteOptions->set_Position(FootnotePosition::BeneathText);
footnoteOptions->set_RestartRule(FootnoteNumberingRule::RestartPage);
footnoteOptions->set_StartNumber(1);

builder->Write(u" Hello again.");
builder->InsertFootnote(FootnoteType::Footnote, u"Endnote reference text.");

// Configure all endnotes in the first section to maintain a continuous count throughout the section,
// starting from 1. Also, set them all to appear collected at the end of the document.
SharedPtr<EndnoteOptions> endnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_EndnoteOptions();
endnoteOptions->set_Position(EndnotePosition::EndOfDocument);
endnoteOptions->set_RestartRule(FootnoteNumberingRule::Continuous);
endnoteOptions->set_StartNumber(1);

doc->Save(ArtifactsDir + u"PageSetup.FootnoteOptions.docx");
```

