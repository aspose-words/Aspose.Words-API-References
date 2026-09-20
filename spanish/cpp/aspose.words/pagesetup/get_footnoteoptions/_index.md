---
title: "Aspose::Words::PageSetup::get_FootnoteOptions método"
linktitle: "get_FootnoteOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_FootnoteOptions método. Proporciona opciones que controlan la numeración y la posición de las notas al pie en esta sección en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words/pagesetup/get_footnoteoptions/
---
## PageSetup::get_FootnoteOptions method


Proporciona opciones que controlan la numeración y la posición de las notas al pie en esta sección.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> Aspose::Words::PageSetup::get_FootnoteOptions()
```


## Ejemplos



Muestra cómo configurar opciones que afectan a las notas al pie/notas finales en una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote reference text.");

// Configure todas las notas al pie en la primera sección para reiniciar la numeración desde 1
// en cada página nueva y mostrarse directamente debajo del texto en cada página.
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> footnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_FootnoteOptions();
footnoteOptions->set_Position(Aspose::Words::Notes::FootnotePosition::BeneathText);
footnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
footnoteOptions->set_StartNumber(1);

builder->Write(u" Hello again.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Endnote reference text.");

// Configure todas las notas finales en la primera sección para mantener un recuento continuo a lo largo de la sección,
// Comenzando desde 1. Además, configure todos para que aparezcan recopilados al final del documento.
System::SharedPtr<Aspose::Words::Notes::EndnoteOptions> endnoteOptions = doc->get_Sections()->idx_get(0)->get_PageSetup()->get_EndnoteOptions();
endnoteOptions->set_Position(Aspose::Words::Notes::EndnotePosition::EndOfDocument);
endnoteOptions->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::Continuous);
endnoteOptions->set_StartNumber(1);

doc->Save(get_ArtifactsDir() + u"PageSetup.FootnoteOptions.docx");
```

## Ver también

* Class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
