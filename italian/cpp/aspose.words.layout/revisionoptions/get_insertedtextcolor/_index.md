---
title: "Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor metodo"
linktitle: "get_InsertedTextColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor metodo. Consente di specificare il colore da utilizzare per il contenuto inserito Insertion. Il valore predefinito è ByAuthor in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.layout/revisionoptions/get_insertedtextcolor/
---
## RevisionOptions::get_InsertedTextColor method


Consente di specificare il colore da utilizzare per il contenuto inserito [Insertion](../../../aspose.words/revisiontype/). Il valore predefinito è [ByAuthor](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor()
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

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
