---
title: "Aspose::Words::Saving::FontSavingArgs class"
linktitle: "FontSavingArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::FontSavingArgs class. Предоставляет данные для события FontSaving(). Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class


Предоставляет данные для события [FontSaving()](../ifontsavingcallback/fontsaving/). Чтобы узнать больше, посетите статью документации [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class FontSavingArgs : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Bold](./get_bold/)() const | Указывает, является ли текущий шрифт полужирным. |
| [get_Document](./get_document/)() const | Получает объект документа, который сохраняется. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Указывает название текущего семейства шрифта. |
| [get_FontFileName](./get_fontfilename/)() const | Получает или задает имя файла (без пути), в который будет сохранён шрифт. |
| [get_FontStream](./get_fontstream/)() const | Позволяет указать поток, в который будет сохранён шрифт. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Позволяет указать, будет ли текущий шрифт экспортирован как ресурс шрифта. По умолчанию **true**. |
| [get_IsSubsettingNeeded](./get_issubsettingneeded/)() const | Позволяет указать, будет ли текущий шрифт подмножеством перед экспортом в виде ресурса шрифта. |
| [get_Italic](./get_italic/)() const | Указывает, является ли текущий шрифт курсивным. |
| [get_KeepFontStreamOpen](./get_keepfontstreamopen/)() const | Указывает, должна ли Aspose.Words оставлять поток открытым или закрывать его после сохранения шрифта. |
| [get_OriginalFileName](./get_originalfilename/)() const | Получает оригинальное имя файла шрифта с расширением. |
| [get_OriginalFileSize](./get_originalfilesize/)() const | Получает оригинальный размер файла шрифта. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FontFileName](./set_fontfilename/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::FontSavingArgs::get_FontFileName](./get_fontfilename/). |
| [set_FontStream](./set_fontstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Сеттер для [Aspose::Words::Saving::FontSavingArgs::get_FontStream](./get_fontstream/). |
| [set_FontStream](./set_fontstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Позволяет указать, будет ли текущий шрифт экспортирован как ресурс шрифта. По умолчанию **true**. |
| [set_IsSubsettingNeeded](./set_issubsettingneeded/)(bool) | Сеттер для [Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded](./get_issubsettingneeded/). |
| [set_KeepFontStreamOpen](./set_keepfontstreamopen/)(bool) | Сеттер для [Aspose::Words::Saving::FontSavingArgs::get_KeepFontStreamOpen](./get_keepfontstreamopen/). |
| static [Type](./type/)() |  |
## Примечания


Когда Aspose.Words сохраняет документ в HTML или связанные форматы и [ExportFontResources](../htmlsaveoptions/get_exportfontresources/) установлен в **true**, он сохраняет каждый шрифт для экспорта в отдельный файл.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

Чтобы решить, сохранять ли конкретный ресурс шрифта, используйте свойство [IsExportNeeded](./get_isexportneeded/).

Чтобы сохранять шрифты в потоки вместо файлов, используйте свойство [FontStream](./get_fontstream/).
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
