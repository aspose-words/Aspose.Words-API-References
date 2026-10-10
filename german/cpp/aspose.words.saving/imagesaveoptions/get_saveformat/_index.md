---
title: "Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat Methode"
linktitle: "get_SaveFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat Methode. Gibt das Format an, in dem die gerenderten Dokumentseiten oder Formen gespeichert werden, wenn dieses Speicheroptionsobjekt verwendet wird. Kann ein Raster‑Tiff, Png, Bmp, Jpeg oder ein Vektor‑Emf, Eps, WebP, Svg in C++ sein."
type: docs
weight: 13000
url: /de/cpp/aspose.words.saving/imagesaveoptions/get_saveformat/
---
## ImageSaveOptions::get_SaveFormat method


Gibt das Format an, in dem die gerenderten Dokumentseiten oder Formen gespeichert werden, wenn dieses Speicheroptionsobjekt verwendet wird. Kann ein Raster‑[Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/) oder ein Vektor‑[Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../), [Svg](../../../aspose.words/saveformat/) sein.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat() override
```

## Hinweise


Die Anzahl der anderen Optionen hängt vom ausgewählten Format ab.

Außerdem ist es möglich, sowohl über [ImageSaveOptions](../) als auch über [SvgSaveOptions](../../svgsaveoptions/) in SVG zu speichern.

## Beispiele



Zeigt, wie das Bild bearbeitet werden kann, während Aspose.Words ein Dokument konvertiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions‑Objekt übergeben, um
// das Bild zu bearbeiten, während der Speichervorgang es rendert.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Wir können diese Eigenschaften anpassen, um die Helligkeit und den Kontrast des Bildes zu ändern.
// Beide liegen auf einer Skala von 0‑1 und haben standardmäßig 0,5.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Wir können die horizontale und vertikale Auflösung mit diesen Eigenschaften anpassen.
// Dies wirkt sich auf die Abmessungen des Bildes aus.
// Der Standardwert für diese Eigenschaften ist 96,0 bei einer Auflösung von 96 dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Wir können das Bild mit dieser Eigenschaft skalieren. Der Standardwert ist 1,0 für eine Skalierung von 100 %.
// Wir können diese Eigenschaft verwenden, um Änderungen der Bildabmessungen, die durch eine Auflösungsänderung entstehen würden, zu neutralisieren.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## Siehe auch

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
