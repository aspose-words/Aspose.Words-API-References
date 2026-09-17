---
title: "Aspose::Words::Fonts::FontInfo::get_IsTrueType méthode"
linktitle: "get_IsTrueType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontInfo::get_IsTrueType méthode. Indique que cette police est une police TrueType ou OpenType, par opposition à une police raster ou vectorielle. La valeur par défaut est true en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fonts/fontinfo/get_istruetype/
---
## FontInfo::get_IsTrueType method


Indique que cette police est une police TrueType ou OpenType par opposition à une police raster ou vectorielle. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Fonts::FontInfo::get_IsTrueType() const
```


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
