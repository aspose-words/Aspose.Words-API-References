---
title: "Aspose::Words::Fonts::FontInfo class"
linktitle: "FontInfo"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontInfo class. Указывает информацию о шрифте, используемом в документе. Чтобы узнать больше, посетите документацию по C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.fonts/fontinfo/
---
## FontInfo class


Указывает информацию о шрифте, используемом в документе. Чтобы узнать больше, посетите статью документации [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfo : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AltName](./get_altname/)() const | Получает или задает альтернативное название шрифта. |
| [get_Charset](./get_charset/)() | Получает или задает набор символов шрифта. |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() | Получает права лицензии встраиваемого шрифта. |
| [get_Family](./get_family/)() const | Получает или задает семейство шрифтов, к которому принадлежит данный шрифт. |
| [get_IsTrueType](./get_istruetype/)() const | Указывает, что этот шрифт является шрифтом TrueType или OpenType, в отличие от растрового или векторного шрифта. По умолчанию **true**. |
| [get_Name](./get_name/)() const | Получает имя шрифта. |
| [get_Panose](./get_panose/)() const | Получает или задает номер классификации гарнитуры PANOSE. |
| [get_Pitch](./get_pitch/)() const | Параметр pitch указывает, является ли шрифт моноширинным, пропорционально распределённым или использует значение по умолчанию. |
| [GetEmbeddedFont](./getembeddedfont/)(Aspose::Words::Fonts::EmbeddedFontFormat, Aspose::Words::Fonts::EmbeddedFontStyle) | Получает конкретный встроенный файл шрифта. |
| [GetEmbeddedFontAsOpenType](./getembeddedfontasopentype/)(Aspose::Words::Fonts::EmbeddedFontStyle) | Получает встроенный файл шрифта в формате OpenType. [Fonts](../) в формате Embedded OpenType преобразуются в OpenType. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AltName](./set_altname/)(const System::String\&) | Сеттер для [Aspose::Words::Fonts::FontInfo::get_AltName](./get_altname/). |
| [set_Charset](./set_charset/)(int32_t) | Сеттер для [Aspose::Words::Fonts::FontInfo::get_Charset](./get_charset/). |
| [set_Family](./set_family/)(Aspose::Words::Fonts::FontFamily) | Сеттер для [Aspose::Words::Fonts::FontInfo::get_Family](./get_family/). |
| [set_IsTrueType](./set_istruetype/)(bool) | Сеттер для [Aspose::Words::Fonts::FontInfo::get_IsTrueType](./get_istruetype/). |
| [set_Panose](./set_panose/)(const System::ArrayPtr\<uint8_t\>\&) | Сеттер для [Aspose::Words::Fonts::FontInfo::get_Panose](./get_panose/). |
| [set_Pitch](./set_pitch/)(Aspose::Words::Fonts::FontPitch) | Сеттер для [Aspose::Words::Fonts::FontInfo::get_Pitch](./get_pitch/). |
| static [Type](./type/)() |  |
## Примечания


Вы не создаёте экземпляры этого класса напрямую. Используйте свойство [FontInfos](../../aspose.words/documentbase/get_fontinfos/) для доступа к коллекции шрифтов, определённых в документе.

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
