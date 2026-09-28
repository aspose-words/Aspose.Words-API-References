---
title: "Aspose::Words::Fonts::FontInfo::get_IsTrueType метод"
linktitle: "get_IsTrueType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontInfo::get_IsTrueType метод. Указывает, что этот шрифт является TrueType или OpenType шрифтом, в отличие от растрового или векторного шрифта. По умолчанию true в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.fonts/fontinfo/get_istruetype/
---
## FontInfo::get_IsTrueType method


Указывает, что этот шрифт является шрифтом TrueType или OpenType, в отличие от растрового или векторного шрифта. По умолчанию **true**.

```cpp
bool Aspose::Words::Fonts::FontInfo::get_IsTrueType() const
```


## Примеры



Показывает, как вывести детали о шрифтах, присутствующих в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Вывести все используемые и неиспользуемые шрифты в документе.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## См. также

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
