---
title: "Aspose::Words::Fonts::FolderFontSource class"
linktitle: "FolderFontSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FolderFontSource class. Представляет папку, содержащую файлы шрифтов TrueType. Чтобы узнать больше, посетите документацию по C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class


Представляет папку, содержащую файлы шрифтов TrueType. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FolderFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Методы

| Метод | Описание |
| --- | --- |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool) | Конструктор. |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool, int32_t) | Конструктор. |
| [get_FolderPath](./get_folderpath/)() const | Путь к папке. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Возвращает приоритет источника шрифтов. |
| [get_ScanSubfolders](./get_scansubfolders/)() const | Определяет, сканировать ли подпапки. |
| [get_Type](./get_type/)() override | Возвращает тип источника шрифтов. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Вызывается во время обработки источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Возвращает список шрифтов, доступных через этот источник. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Вызывается во время обработки источника шрифтов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.
```cpp
// Создайте источник шрифтов из папки, содержащей файлы шрифтов.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## См. также

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
