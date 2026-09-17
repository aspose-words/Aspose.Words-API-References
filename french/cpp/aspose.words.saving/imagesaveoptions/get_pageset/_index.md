---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageSet méthode"
linktitle: "get_PageSet"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageSet méthode. Obtient ou définit les pages à rendre. La valeur par défaut est toutes les pages du document en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/get_pageset/
---
## ImageSaveOptions::get_PageSet method


Obtient ou définit les pages à rendre. La valeur par défaut est toutes les pages du document.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::ImageSaveOptions::get_PageSet()
```

## Remarques


Cette propriété n’a d’effet que lors du rendu des pages du document. Cette propriété est ignorée lors du rendu des formes en images.

## Exemples



Montre comment rendre une page d'un document en image JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Définissez "PageSet" à "1" pour sélectionner la deuxième page via
// l'index basé sur zéro à partir duquel commencer le rendu du document.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Lorsque nous enregistrons le document au format JPEG, Aspose.Words ne rend qu'une seule page.
// Cette image contiendra une page à partir de la page deux,
// qui sera simplement la deuxième page du document original.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```


Montre comment spécifier quelle page d’un document rendre en tant qu’image.
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

// Lorsque nous enregistrons le document en image, Aspose.Words ne rend par défaut que la première page.
// Nous pouvons passer un objet SaveOptions pour spécifier une autre page à rendre.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Gif);
// Rendre chaque page du document dans un fichier image séparé.
for (int32_t i = 1; i <= doc->get_PageCount(); i++)
{
    saveOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageIndex.Page {0}.gif", i), saveOptions);
}
```


Montre comment rendre chaque page d'un document en une image TIFF distincte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Définissez la propriété "PageSet" au numéro de la première page à partir de
    // à partir de laquelle commencer le rendu du document.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Exporter la page à 2325x5325 pixels et 600 dpi.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```


Montre comment extraire des pages en fonction de plages de pages exactes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Voir aussi

* Class [PageSet](../../pageset/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
