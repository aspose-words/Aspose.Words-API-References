---
title: "Aspose::Words::Fonts::PhysicalFontInfo classe"
linktitle: "PhysicalFontInfo"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo classe. Spécifie les informations sur la police physique disponible pour le moteur de polices Aspose.Words. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class


Spécifie les informations sur la police physique disponible pour le moteur de police Aspose.Words. Pour en savoir plus, consultez l'article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class PhysicalFontInfo : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() const | Intégration des droits de licence pour la police. |
| [get_FilePath](./get_filepath/)() const | Chemin vers le fichier de police le cas échéant. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Nom de famille de la police. |
| [get_FullFontName](./get_fullfontname/)() const | Nom complet de la police. |
| [get_Version](./get_version/)() const | Chaîne de version de la police. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exemples



Montre comment lister les polices disponibles.
```cpp
// Configurez Aspose.Words pour récupérer les polices depuis un dossier personnalisé, puis affichez chaque police disponible.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## Voir aussi

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
