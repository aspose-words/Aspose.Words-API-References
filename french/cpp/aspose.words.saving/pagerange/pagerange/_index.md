---
title: "Constructeur Aspose::Words::Saving::PageRange::PageRange"
linktitle: "PageRange"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Constructeur Aspose::Words::Saving::PageRange::PageRange. Crée un nouvel objet de plage de pages en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.saving/pagerange/pagerange/
---
## PageRange::PageRange constructor


Crée un nouvel objet de plage de pages.

```cpp
Aspose::Words::Saving::PageRange::PageRange(int32_t from, int32_t to)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| de | int32_t | L'index de la page de départ basé sur zéro. |
| à | int32_t | L'index de la page de fin basé sur zéro. S'il dépasse l'index de la dernière page du document, il est tronqué pour s'adapter au document lors du rendu. |

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

* Class [PageRange](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
