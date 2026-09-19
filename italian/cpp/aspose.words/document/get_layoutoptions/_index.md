---
title: "Aspose::Words::Document::get_LayoutOptions metodo"
linktitle: "get_LayoutOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_LayoutOptions metodo. Ottiene un oggetto LayoutOptions che rappresenta le opzioni per controllare il processo di layout di questo documento in C++."
type: docs
weight: 36000
url: /it/cpp/aspose.words/document/get_layoutoptions/
---
## Document::get_LayoutOptions method


Ottiene un oggetto [LayoutOptions](../../../aspose.words.layout/layoutoptions/) che rappresenta le opzioni per controllare il processo di layout di questo documento.

```cpp
System::SharedPtr<Aspose::Words::Layout::LayoutOptions> Aspose::Words::Document::get_LayoutOptions() const
```


## Esempi



Mostra come nascondere il testo in un documento di output renderizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci testo nascosto, quindi specifica se desideriamo ometterlo da un documento renderizzato.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


Mostra come visualizzare i segni di paragrafo in un documento di output renderizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi alcuni paragrafi, quindi abilita i segni di paragrafo per mostrare le fine dei paragrafi
// con il simbolo pilcrow (¶) quando renderizziamo il documento.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


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

* Class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
