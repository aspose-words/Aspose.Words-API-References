---
title: "metodo Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing"
linktitle: "get_UseAntiAliasing"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing. Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words.saving/saveoptions/get_useantialiasing/
---
## SaveOptions::get_UseAntiAliasing method


Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing() const
```

## Note


Il valore predefinito è **false**. Quando questo valore è impostato su **true**, l'anti-aliasing viene utilizzato per il rendering.

Questa proprietà è utilizzata quando il documento viene esportato nei seguenti formati: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/). Quando il documento viene esportato nei formati [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) o [Mobi](../../../aspose.words/saveformat/) questa opzione è usata per le immagini raster.

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
