---
title: "Aspose::Words::Saving::ImlRenderingMode enum"
linktitle: "ImlRenderingMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ImlRenderingMode enum. Specifica come gli oggetti inchiostro (InkML) vengono renderizzati in formati di pagina fissi in C++."
type: docs
weight: 66000
url: /it/cpp/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enum


Specifica come gli oggetti ink (InkML) vengono renderizzati nei formati di pagina fissi.

```cpp
enum class ImlRenderingMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Fallback | 0 | Se è disponibile una forma di fallback per l'oggetto inchiostro (InkML), Aspose.Words renderizza la forma di fallback invece dell'InkML. |
| InkML | 1 | Aspose.Words ignora la forma di fallback dell'oggetto inchiostro (InkML) e rende direttamente InkML. Questa è la modalità predefinita. |


## Esempi



Mostra come rendere l'oggetto Ink.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Ink object.docx");

// Imposta 'ImlRenderingMode.InkML' per ignorare la forma di fallback dell'oggetto inchiostro (InkML) e renderizzare direttamente InkML.
// Se il risultato del rendering è insoddisfacente,
// si prega di utilizzare 'ImlRenderingMode.Fallback' per ottenere un risultato simile alle versioni precedenti.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(Aspose::Words::Saving::ImlRenderingMode::InkML);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
