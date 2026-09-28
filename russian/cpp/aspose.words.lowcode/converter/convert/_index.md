---
title: "Aspose::Words::LowCode::Converter::Convert метод"
linktitle: "Конвертировать"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Converter::Convert метод. Преобразует заданный входной документ в один выходной документ, используя указанные входные и выходные потоки в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.lowcode/converter/convert/
---
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Преобразует указанный входной документ в единый выходной документ, используя заданные входные и выходные потоки.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входные потоки. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Параметры загрузки входного документа. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Преобразует указанный входной документ в единый выходной документ, используя заданные входные и выходные потоки.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Преобразует указанный входной документ в единый выходной документ, используя заданные входные и выходные потоки.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входные потоки. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Преобразует указанный входной документ в выходной документ, используя заданные имена входного и выходного файлов и его параметры загрузки/сохранения.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | const System::String\& | Имя входного файла. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Параметры загрузки входного документа. |
| outputFile | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&) method


Преобразует указанный входной документ в выходной документ, используя заданные имена файлов ввода и вывода и их расширения.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | const System::String\& | Имя входного файла. |
| outputFile | const System::String\& | Имя выходного файла. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Преобразует указанный входной документ в выходной документ, используя заданные имена входного и выходного файлов и конечный формат документа.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | const System::String\& | Имя входного файла. |
| outputFile | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Преобразует указанный входной документ в выходной документ, используя заданные имена входного и выходного файлов и параметры сохранения.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | const System::String\& | Имя входного файла. |
| outputFile | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
