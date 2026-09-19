---
title: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate method"
linktitle: "get_DefaultTemplate"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate method. Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è una stringa vuota in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/saveoptions/get_defaulttemplate/
---
## SaveOptions::get_DefaultTemplate method


Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **empty string**.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_DefaultTemplate() const
```


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

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
