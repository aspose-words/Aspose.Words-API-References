---
title: "Metodo Aspose::Words::PageSetup::get_EndnoteOptions"
linktitle: "get_EndnoteOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::PageSetup::get_EndnoteOptions. Fornisce opzioni che controllano la numerazione e il posizionamento delle note finali in questa sezione in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words/pagesetup/get_endnoteoptions/
---
## PageSetup::get_EndnoteOptions method


Fornisce opzioni che controllano la numerazione e il posizionamento delle note finali in questa sezione.

```cpp
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> Aspose::Words::PageSetup::get_EndnoteOptions()
```


## Esempi



Mostra come configurare le opzioni che influenzano le note a piè di pagina/note finali in una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote reference text.");

// Configura tutte le note a piè di pagina nella prima sezione per riavviare la numerazione da 1
// ad ogni nuova pagina e visualizzarle direttamente sotto il testo in ogni pagina.
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> footnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_FootnoteOptions();
footnoteOptions->set_Position(Aspose::Words::Notes::FootnotePosition::BeneathText);
footnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
footnoteOptions->set_StartNumber(1);

builder->Write(u" Hello again.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Endnote reference text.");

// Configura tutte le note finali nella prima sezione per mantenere un conteggio continuo per tutta la sezione,
// a partire da 1. Inoltre, impostali tutti in modo che appaiano raccolti alla fine del documento.
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> endnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_EndnoteOptions();
endnoteOptions->set_Position(Aspose::Words::Notes::EndnotePosition::EndOfDocument);
endnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::Continuous);
endnoteOptions->set_StartNumber(1);

doc->Save(get_ArtifactsDir() + u"PageSetup.FootnoteOptions.docx");
```

## Vedi anche

* Class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
