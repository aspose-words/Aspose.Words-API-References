---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageSet Methode"
linktitle: "get_PageSet"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageSet Methode. Ermittelt oder legt die zu rendernden Seiten fest. Standard ist, dass alle Seiten im Dokument gerendert werden, in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.saving/imagesaveoptions/get_pageset/
---
## ImageSaveOptions::get_PageSet method


Ruft die zu rendernden Seiten ab oder legt sie fest. Standard ist, dass alle Seiten im Dokument gerendert werden.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::ImageSaveOptions::get_PageSet()
```

## Hinweise


Diese Eigenschaft wirkt nur beim Rendern von Dokumentseiten. Diese Eigenschaft wird ignoriert, wenn Formen zu Bildern gerendert werden.

## Beispiele



Zeigt, wie man eine Seite eines Dokuments in ein JPEG‑Bild rendert.
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
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Setzen Sie "PageSet" auf "1", um die zweite Seite auszuwählen über
// den nullbasierten Index, um mit dem Rendern des Dokuments zu beginnen.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Wenn wir das Dokument im JPEG‑Format speichern, rendert Aspose.Words nur eine Seite.
// Dieses Bild enthält eine Seite, beginnend mit Seite zwei,
// die lediglich die zweite Seite des Originaldokuments ist.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```


Zeigt, wie man angibt, welche Seite eines Dokuments als Bild gerendert werden soll.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world! This is page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"This is page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"This is page 3.");

ASSERT_EQ(3, doc->get_PageCount());

// Wenn wir das Dokument als Bild speichern, rendert Aspose.Words standardmäßig nur die erste Seite.
// Wir können ein SaveOptions‑Objekt übergeben, um eine andere Seite zum Rendern anzugeben.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Gif);
// Rendern Sie jede Seite des Dokuments in eine separate Bilddatei.
for (int32_t i = 1; i <= doc->get_PageCount(); i++)
{
    saveOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageIndex.Page {0}.gif", i), saveOptions);
}
```


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


Zeigt, wie Seiten basierend auf genauen PageRanges extrahiert werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Siehe auch

* Class [PageSet](../../pageset/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
