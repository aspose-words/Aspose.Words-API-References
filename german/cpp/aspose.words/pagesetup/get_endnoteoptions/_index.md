---
title: "Aspose::Words::PageSetup::get_EndnoteOptions Methode"
linktitle: "get_EndnoteOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_EndnoteOptions Methode. Stellt Optionen bereit, die die Nummerierung und Positionierung von Endnoten in diesem Abschnitt in C++ steuern."
type: docs
weight: 14000
url: /de/cpp/aspose.words/pagesetup/get_endnoteoptions/
---
## PageSetup::get_EndnoteOptions method


Stellt Optionen bereit, die die Nummerierung und Positionierung von Endnoten in diesem Abschnitt steuern.

```cpp
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> Aspose::Words::PageSetup::get_EndnoteOptions()
```


## Beispiele



Zeigt, wie man Optionen konfiguriert, die Fußnoten/Endnoten in einem Abschnitt betreffen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote reference text.");

// Konfigurieren Sie alle Fußnoten im ersten Abschnitt so, dass die Nummerierung ab 1 neu beginnt
// bei jeder neuen Seite und lassen sie sich direkt unter dem Text auf jeder Seite anzeigen.
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> footnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_FootnoteOptions();
footnoteOptions->set_Position(Aspose::Words::Notes::FootnotePosition::BeneathText);
footnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
footnoteOptions->set_StartNumber(1);

builder->Write(u" Hello again.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Endnote reference text.");

// Konfigurieren Sie alle Endnoten im ersten Abschnitt, um eine durchgehende Zählung über den gesamten Abschnitt beizubehalten,
// beginnend bei 1. Außerdem stellen Sie ein, dass sie alle am Ende des Dokuments gesammelt erscheinen.
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> endnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_EndnoteOptions();
endnoteOptions->set_Position(Aspose::Words::Notes::EndnotePosition::EndOfDocument);
endnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::Continuous);
endnoteOptions->set_StartNumber(1);

doc->Save(get_ArtifactsDir() + u"PageSetup.FootnoteOptions.docx");
```

## Siehe auch

* Class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
