---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor‑Methode"
linktitle: "get_PaperColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor‑Methode. Gibt die Hintergrund‑(Papier‑)Farbe für die erzeugten Bilder zurück oder legt sie fest. Der Standardwert ist Weiß in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.saving/imagesaveoptions/get_papercolor/
---
## ImageSaveOptions::get_PaperColor method


Liest oder setzt die Hintergrundfarbe (Papier) für die erzeugten Bilder. Der Standardwert ist **White**.

```cpp
System::Drawing::Color Aspose::Words::Saving::ImageSaveOptions::get_PaperColor()
```

## Hinweise


Beim Rendern von Seiten eines Dokuments, das seine eigene Hintergrundfarbe festlegt, überschreibt die Dokument‑Hintergrundfarbe die in dieser Eigenschaft angegebene Farbe.

## Beispiele



Rendert eine Seite eines Word‑Dokuments in ein Bild mit transparentem oder farbigem Hintergrund.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Erstellen Sie ein "ImageSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Setzen Sie die \"PaperColor\"-Eigenschaft auf eine transparente Farbe, um eine transparente
// Hintergrund für das Dokument, während es zu einem Bild gerendert wird.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Setzen Sie die \"PaperColor\"-Eigenschaft auf eine undurchsichtige Farbe, um diese Farbe anzuwenden
// als Hintergrund des Dokuments, wenn wir es zu einem Bild rendern.
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

## Siehe auch

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
