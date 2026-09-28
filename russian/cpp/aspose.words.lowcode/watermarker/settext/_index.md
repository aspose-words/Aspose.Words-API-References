---
title: "Aspose::Words::LowCode::Watermarker::SetText метод"
linktitle: "SetText"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Watermarker::SetText метод. Добавляет текстовый водяной знак в документ из потоков с параметрами в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.lowcode/watermarker/settext/
---
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) method


Добавляет текстовый водяной знак в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Добавляет текстовый водяной знак в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Определяет дополнительные параметры для текстового водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Добавляет текстовый водяной знак в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Добавляет текстовый водяной знак в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Определяет дополнительные параметры для текстового водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Определяет дополнительные параметры для текстового водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Определяет дополнительные параметры для текстового водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&) method


Добавляет текстовый водяной знак в документ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetText(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Добавляет текстовый водяной знак в документ с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetText(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkText, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| watermarkText | const System::String\& | Текст, отображаемый в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Определяет дополнительные параметры для текстового водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
