---
title: "Aspose::Words::PageSetup::get_EndnoteOptions-metod"
linktitle: "get_EndnoteOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_EndnoteOptions-metod. Tillhandahåller alternativ som styr numrering och placering av slutnoter i detta avsnitt i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words/pagesetup/get_endnoteoptions/
---
## PageSetup::get_EndnoteOptions method


Tillhandahåller alternativ som styr numrering och placering av slutnoter i detta avsnitt.

```cpp
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> Aspose::Words::PageSetup::get_EndnoteOptions()
```


## Exempel



Visar hur man konfigurerar alternativ som påverkar fotnoter/slutnoter i ett avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote reference text.");

// Konfigurera alla fotnoter i det första avsnittet så att numreringen startar om från 1
// vid varje ny sida och visas direkt under texten på varje sida.
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> footnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_FootnoteOptions();
footnoteOptions->set_Position(Aspose::Words::Notes::FootnotePosition::BeneathText);
footnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
footnoteOptions->set_StartNumber(1);

builder->Write(u" Hello again.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Endnote reference text.");

// Konfigurera alla slutnoter i det första avsnittet så att de behåller en kontinuerlig räkning genom hela avsnittet,
// med start från 1. Ställ också in dem så att de samlas i slutet av dokumentet.
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> endnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_EndnoteOptions();
endnoteOptions->set_Position(Aspose::Words::Notes::EndnotePosition::EndOfDocument);
endnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::Continuous);
endnoteOptions->set_StartNumber(1);

doc->Save(get_ArtifactsDir() + u"PageSetup.FootnoteOptions.docx");
```

## Se även

* Class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
