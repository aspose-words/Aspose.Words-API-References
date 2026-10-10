---
title: "Aspose::Words::Document::get_AttachedTemplate metodo"
linktitle: "get_AttachedTemplate"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_AttachedTemplate metodo. Ottiene o imposta il percorso completo del modello allegato al documento in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words/document/get_attachedtemplate/
---
## Document::get_AttachedTemplate method


Ottiene o imposta il percorso completo del modello allegato al documento.

```cpp
System::String Aspose::Words::Document::get_AttachedTemplate()
```

## Note


Una stringa vuota indica che il documento è allegato al modello Normal.

## Esempi



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
