---
title: "Aspose::Words::LowCode::Watermarker::SetImage метод"
linktitle: "SetImage"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Watermarker::SetImage метод. Добавляет изображение водяного знака в документ из потоков с параметрами в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.lowcode/watermarker/setimage/
---
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) method


Добавляет изображение водяного знака в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Изображение, отображаемое в виде водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Изображение, отображаемое в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) method


Добавляет изображение водяного знака в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток изображения, отображаемый как водяной знак. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток изображения, отображаемый как водяной знак. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) method


Добавляет изображение водяного знака в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Изображение, отображаемое в виде водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Изображение, отображаемое в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Добавляет изображение водяного знака в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток изображения, отображаемый как водяной знак. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ из потоков с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Поток изображения, отображаемый как водяной знак. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Добавляет изображение водяного знака в документ с параметрами и указанным форматом сохранения.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| watermarkImageFileName | const System::String\& | Изображение, отображаемое в виде водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ с параметрами и указанным форматом сохранения.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| watermarkImageFileName | const System::String\& | Изображение, отображаемое в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Добавляет изображение водяного знака в документ с параметрами и указанным форматом сохранения.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| watermarkImageFileName | const System::String\& | Изображение, отображаемое в виде водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ с параметрами и указанным форматом сохранения.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| watermarkImageFileName | const System::String\& | Изображение, отображаемое в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&) method


Добавляет изображение водяного знака в документ.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| watermarkImageFileName | const System::String\& | Изображение, отображаемое в виде водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Добавляет изображение водяного знака в документ с параметрами.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| watermarkImageFileName | const System::String\& | Изображение, отображаемое в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Определяет дополнительные параметры для изображений водяного знака. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
