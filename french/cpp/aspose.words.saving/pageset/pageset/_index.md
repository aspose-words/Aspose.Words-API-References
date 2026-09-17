---
title: "Constructeur Aspose::Words::Saving::PageSet::PageSet"
linktitle: "PageSet"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Constructeur Aspose::Words::Saving::PageSet::PageSet. Crée un ensemble de pages basé sur des indices de pages exacts en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/pageset/pageset/
---
## PageSet::PageSet(const System::ArrayPtr\<int32_t\>\&) constructor


Crée un ensemble de pages basé sur des indices de pages exacts.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<int32_t> &pages)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| pages | const System::ArrayPtr\<int32_t\>\& | Indices des pages basés sur zéro. |

## Exemples



Montre comment extraire des pages en fonction d'indices de page exacts.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez cinq pages au document.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Créez un objet "XpsSaveOptions", que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// Utilisez la propriété "PageSet" pour sélectionner un ensemble de pages du document à enregistrer dans le XPS de sortie.
// Dans ce cas, nous choisirons, via un indice zéro basé, seulement trois pages : page 1, page 2 et page 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## Voir aussi

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) constructor


Crée un ensemble de pages basé sur des plages.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Saving::PageRange>> &ranges)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| plages | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\& | Tableau de plages de pages. |

## Exemples



Montre comment extraire des pages en fonction de plages de pages exactes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Voir aussi

* Class [PageRange](../../pagerange/)
* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(int32_t) constructor


Crée un ensemble d'une page basé sur l'index de page exact.

```cpp
Aspose::Words::Saving::PageSet::PageSet(int32_t page)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| page | int32_t | Indice de la page basé sur zéro. |

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

## Voir aussi

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
