---
title: "Aspose::Words::Document::get_AutomaticallyUpdateStyles metodo"
linktitle: "get_AutomaticallyUpdateStyles"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_AutomaticallyUpdateStyles metodo. Ottiene o imposta un flag che indica se gli stili nel documento vengono aggiornati per corrispondere agli stili nel modello allegato ogni volta che il documento viene aperto in MS Word in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words/document/get_automaticallyupdatestyles/
---
## Document::get_AutomaticallyUpdateStyles method


Ottiene o imposta un flag che indica se gli stili nel documento vengono aggiornati per corrispondere agli stili del modello allegato ogni volta che il documento viene aperto in MS Word.

```cpp
bool Aspose::Words::Document::get_AutomaticallyUpdateStyles()
```


## Esempi



Mostra come allegare un modello a un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// I documenti Microsoft Word, per impostazione predefinita, includono un modello allegato chiamato "Normal.dotm".
// Non esiste un modello predefinito per i documenti vuoti di Aspose.Words.
ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Allega un modello, quindi imposta il flag per applicare le modifiche di stile
// all'interno del modello agli stili nel nostro documento.
doc->set_AttachedTemplate(get_MyDir() + u"Business brochure.dotx");
doc->set_AutomaticallyUpdateStyles(true);

doc->Save(get_ArtifactsDir() + u"Document.AutomaticallyUpdateStyles.docx");
```


Mostra come impostare un modello predefinito per i documenti che non hanno modelli allegati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Abilita l'aggiornamento automatico degli stili, ma non allegare un documento modello.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Poiché non esiste un documento modello, il documento non aveva alcun luogo dove tenere traccia delle modifiche di stile.
// Utilizza un oggetto SaveOptions per impostare automaticamente un modello
// se un documento che stiamo salvando non ne ha uno.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
