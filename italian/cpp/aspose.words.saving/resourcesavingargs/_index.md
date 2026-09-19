---
title: "Aspose::Words::Saving::ResourceSavingArgs class"
linktitle: "ResourceSavingArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ResourceSavingArgs class. Fornisce dati per l'evento ResourceSaving(). Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 27000
url: /it/cpp/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class


Fornisce dati per l'evento [ResourceSaving()](../iresourcesavingcallback/resourcesaving/). Per saperne di più, visita l'articolo di documentazione [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ResourceSavingArgs : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Document](./get_document/)() const | Ottiene l'oggetto documento che è attualmente in fase di salvataggio. |
| [get_KeepResourceStreamOpen](./get_keepresourcestreamopen/)() const | Specifica se Aspose.Words deve mantenere il flusso aperto o chiuderlo dopo aver salvato una risorsa. |
| [get_ResourceFileName](./get_resourcefilename/)() const | Ottiene o imposta il nome del file (senza percorso) in cui la risorsa verrà salvata. |
| [get_ResourceFileUri](./get_resourcefileuri/)() const | Ottiene o imposta l'identificatore uniforme di risorsa (URI) utilizzato per fare riferimento al file della risorsa dal documento. |
| [get_ResourceStream](./get_resourcestream/)() const | Consente di specificare il flusso in cui la risorsa verrà salvata. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_KeepResourceStreamOpen](./set_keepresourcestreamopen/)(bool) | Impostatore per [Aspose::Words::Saving::ResourceSavingArgs::get_KeepResourceStreamOpen](./get_keepresourcestreamopen/). |
| [set_ResourceFileName](./set_resourcefilename/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName](./get_resourcefilename/). |
| [set_ResourceFileUri](./set_resourcefileuri/)(const System::String\&) | Impostatore per [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri](./get_resourcefileuri/). |
| [set_ResourceStream](./set_resourcestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Impostatore per [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream](./get_resourcestream/). |
| [set_ResourceStream](./set_resourcestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Note


Per impostazione predefinita, quando Aspose.Words salva un documento in HTML a pagina fissa, SVG o Markdown, salva ogni risorsa in un file separato. Aspose.Words utilizza il nome del file del documento e un numero univoco per generare un nome file unico per ogni risorsa trovata nel documento.

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

Per applicare la tua logica nella generazione dei nomi file delle risorse, utilizza la proprietà [ResourceFileName](./get_resourcefilename/).

Per salvare le risorse in flussi invece che in file, utilizza la proprietà [ResourceStream](./get_resourcestream/).
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
