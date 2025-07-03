---
title: Aspose::Words::PageSetup::get_EndnoteOptions method
linktitle: get_EndnoteOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_EndnoteOptions method. Provides options that control numbering and positioning of endnotes in this section in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words/pagesetup/get_endnoteoptions/
---
## PageSetup::get_EndnoteOptions method


Provides options that control numbering and positioning of endnotes in this section.

```cpp
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> Aspose::Words::PageSetup::get_EndnoteOptions()
```


## Examples



Shows how to configure options affecting footnotes/endnotes in a section. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote reference text.");

// Configure all footnotes in the first section to restart the numbering from 1
// at each new page and display themselves directly beneath the text on every page.
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> footnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_FootnoteOptions();
footnoteOptions->set_Position(Aspose::Words::Notes::FootnotePosition::BeneathText);
footnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
footnoteOptions->set_StartNumber(1);

builder->Write(u" Hello again.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Endnote reference text.");

// Configure all endnotes in the first section to maintain a continuous count throughout the section,
// starting from 1. Also, set them all to appear collected at the end of the document.
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> endnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_EndnoteOptions();
endnoteOptions->set_Position(Aspose::Words::Notes::EndnotePosition::EndOfDocument);
endnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::Continuous);
endnoteOptions->set_StartNumber(1);

doc->Save(get_ArtifactsDir() + u"PageSetup.FootnoteOptions.docx");
```

## See Also

* Class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
