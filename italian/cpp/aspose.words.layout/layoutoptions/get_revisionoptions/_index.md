---
title: "Metodo Aspose::Words::Layout::LayoutOptions::get_RevisionOptions"
linktitle: "get_RevisionOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Layout::LayoutOptions::get_RevisionOptions. Ottiene le opzioni di revisione in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.layout/layoutoptions/get_revisionoptions/
---
## LayoutOptions::get_RevisionOptions method


Ottiene le opzioni di revisione.

```cpp
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> Aspose::Words::Layout::LayoutOptions::get_RevisionOptions() const
```


## Esempi



Mostra come modificare l'aspetto delle revisioni in un documento di output renderizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una revisione, quindi cambia il colore di tutte le revisioni in verde.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Rimuovi la barra che appare a sinistra di ogni riga revisionata.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Vedi anche

* Class [RevisionOptions](../../revisionoptions/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
