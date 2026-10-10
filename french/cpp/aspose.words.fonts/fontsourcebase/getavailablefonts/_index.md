---
title: "Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts méthode"
linktitle: "GetAvailableFonts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts méthode. Retourne la liste des polices disponibles via cette source en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase::GetAvailableFonts method


Renvoie la liste des polices disponibles via cette source.

```cpp
System::SharedPtr<System::Collections::Generic::IList<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>>> Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts()
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

* Class [PhysicalFontInfo](../../physicalfontinfo/)
* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
