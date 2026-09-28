---
title: "Aspose::Words::Fonts::PhysicalFontInfo class"
linktitle: "PhysicalFontInfo"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo class. Указывает информацию о физическом шрифте, доступном движку шрифтов Aspose.Words. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class


Указывает информацию о физическом шрифте, доступном движку шрифтов Aspose.Words. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class PhysicalFontInfo : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() const | Встраивание прав лицензирования для шрифта. |
| [get_FilePath](./get_filepath/)() const | Путь к файлу шрифта, если он есть. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Семейное имя шрифта. |
| [get_FullFontName](./get_fullfontname/)() const | Полное имя шрифта. |
| [get_Version](./get_version/)() const | Строка версии шрифта. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Примеры



Показывает, как перечислить доступные шрифты.
```cpp
// Настройте Aspose.Words для получения шрифтов из пользовательской папки, а затем выведите каждый доступный шрифт.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## См. также

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
