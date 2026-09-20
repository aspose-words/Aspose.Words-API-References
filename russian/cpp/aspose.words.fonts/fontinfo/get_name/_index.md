---
title: "Aspose::Words::Fonts::FontInfo::get_Name метод"
linktitle: "get_Name"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontInfo::get_Name метод. Получает имя шрифта в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.fonts/fontinfo/get_name/
---
## FontInfo::get_Name method


Получает имя шрифта.

```cpp
System::String Aspose::Words::Fonts::FontInfo::get_Name() const
```

## Примечания


Не может быть **null**. Может быть пустой строкой.

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
