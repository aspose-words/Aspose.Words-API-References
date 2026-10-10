---
title: "Aspose::Words::Fonts::FontInfo::get_Name metod"
linktitle: "get_Name"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfo::get_Name metod. Hämtar teckensnittets namn i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.fonts/fontinfo/get_name/
---
## FontInfo::get_Name method


Hämtar teckensnittets namn.

```cpp
System::String Aspose::Words::Fonts::FontInfo::get_Name() const
```

## Anmärkningar


Kan inte vara **null**. Kan vara en tom sträng.

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
