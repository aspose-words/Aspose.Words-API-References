---
title: "Metodo Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat. Specifica il formato in cui le pagine o le forme del documento renderizzato saranno salvate se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere un raster Tiff, Png, Bmp, Jpeg o un vettoriale Emf, Eps, WebP, Svg in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.saving/imagesaveoptions/get_saveformat/
---
## ImageSaveOptions::get_SaveFormat method


Specifică il formato in cui le pagine o le forme del documento renderizzato saranno salvate se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere un raster [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/) o un vettoriale [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../), [Svg](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat() override
```

## Note


Il numero di altre opzioni dipende dal formato selezionato.

Inoltre, è possibile salvare in SVG sia tramite [ImageSaveOptions](../) sia tramite [SvgSaveOptions](../../svgsaveoptions/).

## Esempi



Mostra come modificare l'immagine mentre Aspose.Words converte un documento in una.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// modifica l'immagine mentre l'operazione di salvataggio la rende.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Possiamo regolare queste proprietà per modificare la luminosità e il contrasto dell'immagine.
// Entrambe sono su una scala da 0 a 1 e sono impostate a 0.5 per impostazione predefinita.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Possiamo regolare la risoluzione orizzontale e verticale con queste proprietà.
// Ciò influenzerà le dimensioni dell'immagine.
// Il valore predefinito per queste proprietà è 96.0, per una risoluzione di 96dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Possiamo ridimensionare l'immagine usando questa proprietà. Il valore predefinito è 1.0, per una scala del 100%.
// Possiamo usare questa proprietà per annullare eventuali modifiche alle dimensioni dell'immagine che il cambiamento della risoluzione potrebbe causare.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
