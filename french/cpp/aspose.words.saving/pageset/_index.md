---
title: "Classe Aspose::Words::Saving::PageSet"
linktitle: "PageSet"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Saving::PageSet. Décrit un ensemble aléatoire de pages. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words.saving/pageset/
---
## PageSet class


Décrit un ensemble aléatoire de pages. Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSet : public System::Collections::Generic::IEnumerable<int32_t>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [get_All](./get_all/)() | Obtient un ensemble contenant toutes les pages du document dans leur ordre d'origine. |
| static [get_Even](./get_even/)() | Obtient un ensemble contenant toutes les pages paires du document dans leur ordre d'origine. |
| static [get_Odd](./get_odd/)() | Obtient un ensemble contenant toutes les pages impaires du document dans leur ordre d'origine. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSet](./pageset/)(int32_t) | Crée un ensemble d'une page basé sur l'index de page exact. |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | Crée un ensemble de pages basé sur des indices de pages exacts. |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | Crée un ensemble de pages basé sur des plages. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
