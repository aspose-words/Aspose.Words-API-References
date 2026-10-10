---
title: "Aspose::Words::Fonts::FontInfo::get_IsTrueType Methode"
linktitle: "get_IsTrueType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontInfo::get_IsTrueType Methode. Gibt an, dass diese Schriftart eine TrueType- oder OpenType-Schriftart ist, im Gegensatz zu einer Raster- oder Vektorschrift. Standard ist true in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.fonts/fontinfo/get_istruetype/
---
## FontInfo::get_IsTrueType method


Gibt an, dass diese Schrift eine TrueType- oder OpenType-Schrift ist, im Gegensatz zu einer Raster- oder Vektorschrift. Standardwert ist **true**.

```cpp
bool Aspose::Words::Fonts::FontInfo::get_IsTrueType() const
```


## Beispiele



Zeigt, wie man die Details der im Dokument vorhandenen Schriften ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Gibt alle verwendeten und nicht verwendeten Schriften im Dokument aus.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Siehe auch

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
