---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_FontFamilyName méthode"
linktitle: "get_FontFamilyName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_FontFamilyName méthode. Nom de famille de la police en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fonts/physicalfontinfo/get_fontfamilyname/
---
## PhysicalFontInfo::get_FontFamilyName method


Nom de famille de la police.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FontFamilyName() const
```


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

* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
