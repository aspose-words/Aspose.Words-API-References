---
title: "classe Aspose::Words::Saving::PageRange"
linktitle: "PageRange"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Saving::PageRange. Représente une plage continue de pages. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.saving/pagerange/
---
## PageRange class


Représente une plage continue de pages. Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageRange : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageRange](./pagerange/)(int32_t, int32_t) | Crée un nouvel objet de plage de pages. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
