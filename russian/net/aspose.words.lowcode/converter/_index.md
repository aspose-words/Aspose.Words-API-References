---
title: Converter Class
linktitle: Converter
articleTitle: Converter
second_title: Aspose.Words для .NET
description: Легко конвертируйте различные типы документов с помощью Aspose.Words.LowCode.Converter. Упростите свой рабочий процесс, используя всего одну строку кода для бесшовной интеграции.
type: docs
weight: 4230
url: /ru/net/aspose.words.lowcode/converter/
---
## Converter class

Представляет собой группу методов, предназначенных для преобразования различных типов документов с помощью одной строки кода.

```csharp
public class Converter : Processor
```

## Методы

| Имя | Описание |
| --- | --- |
| static [Create](../../aspose.words.lowcode/converter/create/#create)() | Создает новый экземпляр процессора преобразователя. |
| static [Create](../../aspose.words.lowcode/converter/create/#create_1)(*[ConverterContext](../convertercontext/)*) | Создает новый экземпляр процессора преобразователя. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Выполнить действие процессора. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Указывает входной документ для обработки. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает список выходных потоков документов. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной поток для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Указывает выходной файл для процессора. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Указывает выходной файл для процессора. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_4)(*string, string*) | Преобразует заданный входной документ в выходной документ, используя указанные имена входных/выходных файлов и их расширения. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Преобразует заданный входной документ в один выходной документ, используя указанные входные и выходные потоки. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Преобразует заданный входной документ в один выходной документ, используя указанные входные и выходные потоки. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Преобразует заданный входной документ в выходной документ, используя указанные имена входных/выходных файлов и формат конечного документа. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Преобразует заданный входной документ в выходной документ, используя указанные имена входных/выходных файлов и параметры сохранения. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Преобразует заданный входной документ в один выходной документ, используя указанные входные и выходные потоки. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Преобразует заданный входной документ в выходной документ, используя указанные имена входных и выходных файлов и параметры загрузки/сохранения. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_1)(*[Document](../../aspose.words/document/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Преобразует страницы указанного документа в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages)(*[Document](../../aspose.words/document/), [SaveFormat](../../aspose.words/saveformat/)*) | Преобразует страницы указанного документа в изображения указанного формата и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_4)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Преобразует страницы указанного входного потока в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_3)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Преобразует страницы указанного входного потока в изображения в указанном формате и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_6)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Преобразует страницы указанного входного файла в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_5)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Преобразует страницы указанного входного файла в изображения указанного формата и возвращает массив потоков, содержащих изображения. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Преобразует страницы указанного входного потока в изображения, используя предоставленные параметры загрузки и сохранения, и возвращает массив потоков, содержащих изображения. |

## Примечания

Указанные входные и выходные файлы или потоки, а также желаемый формат сохранения используются для преобразования заданного входного документа одного формата в выходной документ другого указанного формата.

Функция конвертации поддерживает более 35 различных форматов файлов.

The[`ConvertToImages`](./converttoimages/)Группа методов предназначена для преобразования документов в изображения, , при этом каждая страница преобразуется в отдельный файл изображения. Эти методы также преобразуют PDF-документы напрямую в форматы с фиксированной страницей , не загружая их в модель документа, что повышает как производительность, так и точность.

С[`PageSet`](../../aspose.words.saving/imagesaveoptions/pageset/), вы можете указать определенный набор страниц для преобразования в изображения.

### Смотрите также

* class [Processor](../processor/)
* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
