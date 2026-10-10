---
title: "Aspose::Words::Fonts::FontInfo::get_Name méthode"
linktitle: "get_Name"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontInfo::get_Name method. Obtient le nom de la police en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.fonts/fontinfo/get_name/
---
## FontInfo::get_Name method


Obtient le nom de la police.

```cpp
System::String Aspose::Words::Fonts::FontInfo::get_Name() const
```

## Remarques


Ne peut pas être **null**. Peut être une chaîne vide.

## Exemples



Montre comment imprimer les détails des polices présentes dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Imprime toutes les polices utilisées et non utilisées dans le document.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Voir aussi

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
