---
title: "Aspose::Words::Fonts::FontInfo::get_IsTrueType metod"
linktitle: "get_IsTrueType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfo::get_IsTrueType metod. Anger att detta teckensnitt är ett TrueType- eller OpenType-teckensnitt till skillnad från ett raster- eller vektorteckensnitt. Standard är true i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.fonts/fontinfo/get_istruetype/
---
## FontInfo::get_IsTrueType method


Indikerar att detta teckensnitt är ett TrueType- eller OpenType-teckensnitt till skillnad från ett raster- eller vektorteckensnitt. Standard är **true**.

```cpp
bool Aspose::Words::Fonts::FontInfo::get_IsTrueType() const
```


## Exempel



Visar hur man skriver ut detaljerna för vilka teckensnitt som finns i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Skriv ut alla använda och oanvända teckensnitt i dokumentet.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Se även

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
