---
title: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode method"
linktitle: "get_ImlRenderingMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode method. Ottiene o imposta un valore che determina come gli oggetti inchiostro (InkML) vengono renderizzati in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.saving/saveoptions/get_imlrenderingmode/
---
## SaveOptions::get_ImlRenderingMode method


Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti inchiostro (InkML).

```cpp
Aspose::Words::Saving::ImlRenderingMode Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode() const
```

## Note


Il valore predefinito è [InkML](../../imlrenderingmode/).

Questa proprietà è utilizzata quando il documento viene esportato in formati a pagina fissa.

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

* Enum [ImlRenderingMode](../../imlrenderingmode/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
