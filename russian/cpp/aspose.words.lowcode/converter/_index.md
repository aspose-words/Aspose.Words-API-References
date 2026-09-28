---
title: "Класс Aspose::Words::LowCode::Converter"
linktitle: "Converter"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::LowCode::Converter. Представляет группу методов, предназначенных для конвертации различных типов документов с помощью одной строки кода в C++."
type: docs
weight: 600
url: /ru/cpp/aspose.words.lowcode/converter/
---
## Converter class


Представляет набор методов, предназначенных для преобразования различных типов документов с помощью одной строки кода.

```cpp
class Converter : public Aspose::Words::LowCode::Processor
```

## Методы

| Метод | Описание |
| --- | --- |
| static [Convert](./convert/)(const System::String\&, const System::String\&) | Преобразует указанный входной документ в выходной документ, используя заданные имена файлов ввода и вывода и их расширения. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Преобразует указанный входной документ в выходной документ, используя заданные имена входного и выходного файлов и конечный формат документа. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Преобразует указанный входной документ в выходной документ, используя заданные имена входного и выходного файлов и параметры сохранения. |
| static [Convert](./convert/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Преобразует указанный входной документ в выходной документ, используя заданные имена входного и выходного файлов и его параметры загрузки/сохранения. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Преобразует указанный входной документ в единый выходной документ, используя заданные входные и выходные потоки. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Преобразует указанный входной документ в единый выходной документ, используя заданные входные и выходные потоки. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Преобразует указанный входной документ в единый выходной документ, используя заданные входные и выходные потоки. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&) | Преобразует страницы указанного входного файла в файлы изображений. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Преобразует страницы указанного входного файла в файлы изображений в заданном формате. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Преобразует страницы указанного входного файла в файлы изображений, используя заданные параметры сохранения. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Преобразует страницы указанного входного файла в файлы изображений, используя предоставленные параметры загрузки и сохранения. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, Aspose::Words::SaveFormat) | Преобразует страницы указанного входного файла в изображения в заданном формате и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Преобразует страницы указанного входного файла в изображения, используя заданные параметры сохранения, и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Преобразует страницы указанного входного потока в изображения в заданном формате и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Преобразует страницы указанного входного потока в изображения, используя заданные параметры сохранения, и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Преобразует страницы указанного входного потока в изображения, используя предоставленные параметры загрузки и сохранения, и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) | Преобразует страницы указанного документа в изображения в заданном формате и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Преобразует страницы указанного документа в изображения, используя заданные параметры сохранения, и возвращает массив потоков, содержащих изображения. |
| static [Create](./create/)() | Создает новый экземпляр процессора конвертера. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ConverterContext\>\&) | Создает новый экземпляр процессора конвертера. |
| [Execute](../processor/execute/)() | Выполнить действие процессора. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Выполнить действие процессора, позволяя отменить задачу обработки документа с использованием указанного токена отмены. |
| [From](../processor/from/)(const System::String\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](../processor/to/)(const System::String\&) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Указывает выходной поток для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Указывает выходной поток для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Примечания


Указанные входные и выходные файлы или потоки, вместе с желаемым форматом сохранения, используются для преобразования данного входного документа из одного формата в выходной документ в другом указанном формате.

Функциональность преобразования поддерживает более 35 различных форматов файлов.

Группа методов [ConvertToImages()](../) предназначена для преобразования документов в изображения, при этом каждая страница преобразуется в отдельный файл изображения. Эти методы также преобразуют PDF‑документы напрямую в форматы фиксированных страниц без загрузки их в модель документа, что повышает как производительность, так и точность.

С помощью [PageSet](../../aspose.words.saving/imagesaveoptions/get_pageset/) можно указать конкретный набор страниц для преобразования в изображения.
## См. также

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
