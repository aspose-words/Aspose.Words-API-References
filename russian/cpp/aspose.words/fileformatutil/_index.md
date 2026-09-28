---
title: "Aspose::Words::FileFormatUtil класс"
linktitle: "FileFormatUtil"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::FileFormatUtil класс. Предоставляет вспомогательные методы для работы с форматами файлов, такие как определение формата файла или преобразование расширений файлов в/из перечислений форматов файлов. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 28000
url: /ru/cpp/aspose.words/fileformatutil/
---
## FileFormatUtil class


Предоставляет вспомогательные методы для работы с файловыми форматами, такие как определение формата файла или преобразование расширений файлов в/из перечислений форматов файлов. Чтобы узнать больше, посетите статью документации [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatUtil
```

## Методы

| Метод | Описание |
| --- | --- |
| static [ContentTypeToLoadFormat](./contenttypetoloadformat/)(const System::String\&) | Преобразует тип содержимого IANA в перечисляемое значение формата загрузки. |
| static [ContentTypeToSaveFormat](./contenttypetosaveformat/)(const System::String\&) | Преобразует тип содержимого IANA в перечисляемое значение формата сохранения. |
| static [DetectFileFormat](./detectfileformat/)(const System::String\&) | Определяет и возвращает информацию о формате документа, хранящегося в дисковом файле. |
| static [DetectFileFormat](./detectfileformat/)(const System::SharedPtr\<System::IO::Stream\>\&) | Определяет и возвращает информацию о формате документа, хранящегося в потоке. |
| static [DetectFileFormat](./detectfileformat/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [ExtensionToSaveFormat](./extensiontosaveformat/)(const System::String\&) | Преобразует расширение имени файла в значение [SaveFormat](../saveformat/). |
| [FileFormatUtil](./fileformatutil/)() |  |
| static [ImageTypeToExtension](./imagetypetoextension/)(Aspose::Words::Drawing::ImageType) | Преобразует перечисляемое значение типа изображения Aspose.Words в расширение файла. Возвращаемое расширение — строка в нижнем регистре с ведущей точкой. |
| static [LoadFormatToExtension](./loadformattoextension/)(Aspose::Words::LoadFormat) | Преобразует перечисляемое значение формата загрузки в расширение файла. Возвращаемое расширение — строка в нижнем регистре с ведущей точкой. |
| static [LoadFormatToSaveFormat](./loadformattosaveformat/)(Aspose::Words::LoadFormat) | Преобразует значение [LoadFormat](../loadformat/) в значение [SaveFormat](../saveformat/), если это возможно. |
| static [SaveFormatToExtension](./saveformattoextension/)(Aspose::Words::SaveFormat) | Преобразует перечисляемое значение формата сохранения в расширение файла. Возвращаемое расширение — строка в нижнем регистре с ведущей точкой. |
| static [SaveFormatToLoadFormat](./saveformattoloadformat/)(Aspose::Words::SaveFormat) | Преобразует значение [SaveFormat](../saveformat/) в значение [LoadFormat](../loadformat/), если это возможно. |

## Примеры



Показывает, как определить кодировку в HTML‑файле.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// Свойство Encoding используется только при создании объекта FileFormatInfo для html‑документа.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
