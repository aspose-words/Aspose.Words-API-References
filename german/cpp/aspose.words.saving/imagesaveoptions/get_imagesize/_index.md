---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize Methode"
linktitle: "get_ImageSize"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize Methode. Gibt die Größe eines erzeugten Bildes in Pixeln zurück oder legt sie fest in C++."
type: docs
weight: 7500
url: /de/cpp/aspose.words.saving/imagesaveoptions/get_imagesize/
---
## ImageSaveOptions::get_ImageSize method


Liest oder setzt die Größe eines erzeugten Bildes in Pixeln.

```cpp
System::Drawing::Size Aspose::Words::Saving::ImageSaveOptions::get_ImageSize() const
```

## Hinweise


Diese Eigenschaft wirkt nur beim Speichern in Rasterbildformate.

Der Standardwert ist (0 x 0), was bedeutet, dass die Größe des erzeugten Bildes anhand der Bildgröße in Punkten, der angegebenen Auflösung und dem Maßstab berechnet wird.

## Beispiele



Zeigt, wie man jede Seite eines Dokuments in ein separates TIFF‑Bild rendert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Erstellen Sie ein "ImageSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Setzen Sie die "PageSet"-Eigenschaft auf die Nummer der ersten Seite von
    // von der aus das Dokument gerendert werden soll.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Exportiere Seite mit 2325x5325 Pixeln und 600 dpi.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```

## Siehe auch

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
