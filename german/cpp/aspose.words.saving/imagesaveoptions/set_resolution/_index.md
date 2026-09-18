---
title: "Aspose::Words::Saving::ImageSaveOptions::set_Resolution Methode"
linktitle: "set_Resolution"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::set_Resolution Methode. Legt sowohl die horizontale als auch die vertikale Auflösung für die erzeugten Bilder fest, in Punkten pro Zoll in C++."
type: docs
weight: 30000
url: /de/cpp/aspose.words.saving/imagesaveoptions/set_resolution/
---
## ImageSaveOptions::set_Resolution method


Legt sowohl die horizontale als auch die vertikale Auflösung für die generierten Bilder in DPI (Punkte pro Zoll) fest.

```cpp
void Aspose::Words::Saving::ImageSaveOptions::set_Resolution(float value)
```

## Hinweise


Diese Eigenschaft wirkt nur beim Speichern in Rasterbildformate.

## Beispiele



Zeigt, wie man eine Auflösung beim Rendern eines Dokuments zu PNG angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Erstellen Sie ein "ImageSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Setzen Sie die \"Resolution\"-Eigenschaft auf \"72\", um das Dokument mit 72 dpi zu rendern.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// Setzen Sie die \"Resolution\"-Eigenschaft auf \"300\", um das Dokument mit 300 dpi zu rendern.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## Siehe auch

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
