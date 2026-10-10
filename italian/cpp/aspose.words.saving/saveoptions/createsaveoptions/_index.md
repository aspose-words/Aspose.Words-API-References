---
title: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions metodo"
linktitle: "CreateSaveOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::SaveOptions::CreateSaveOptions. Crea un oggetto di opzioni di salvataggio di una classe adatta al formato di salvataggio specificato in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.saving/saveoptions/createsaveoptions/
---
## SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat) method


Crea un oggetto di opzioni di salvataggio di una classe adatta al formato di salvataggio specificato.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Il formato di salvataggio per il quale creare un oggetto di opzioni di salvataggio. |

### ReturnValue

Un oggetto di una classe che deriva da [SaveOptions](../).

## Vedi anche

* Class [SaveOptions](../)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## SaveOptions::CreateSaveOptions(const System::String\&) method


Crea un oggetto di opzioni di salvataggio di una classe adatta all'estensione del file specificata nel nome del file fornito.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | L'estensione di questo nome file determina la classe dell'oggetto di opzioni di salvataggio da creare. |

### ReturnValue

Un oggetto di una classe che deriva da [SaveOptions](../).

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
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
