---
title: "Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering method"
linktitle: "get_UseHighQualityRendering"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering method. Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering ad alta qualità (cioè lenti) in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words.saving/saveoptions/get_usehighqualityrendering/
---
## SaveOptions::get_UseHighQualityRendering method


Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering ad alta qualità (cioè lenti).

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering() const
```

## Note


Il valore predefinito è **false**.

Questa proprietà è utilizzata quando il documento viene esportato in formati immagine: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/).

## Esempi



Mostra come migliorare la qualità di un documento renderizzato con [SaveOptions](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```

## Vedi anche

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
