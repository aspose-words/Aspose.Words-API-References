---
title: "Aspose::Words::LowCode::Comparer::Compare метод"
linktitle: "Compare"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Comparer::Compare метод. Сравнивает два документа, загруженных из потоков с дополнительными параметрами, и сохраняет различия в предоставленный поток вывода в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.lowcode/comparer/compare/
---
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Сравнивает два документа, загруженных из потоков, с дополнительными параметрами и сохраняет различия в предоставленный выходной поток в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Оригинальный документ. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Изменённый документ. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Сравнивает два документа, загруженных из потоков, с дополнительными параметрами и сохраняет различия в предоставленный выходной поток в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Оригинальный документ. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Изменённый документ. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) опции сравнения. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Сравнивает два документа, загруженных из потоков, с дополнительными параметрами и сохраняет различия в предоставленный выходной поток в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Оригинальный документ. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Изменённый документ. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Сравнивает два документа, загруженных из потоков, с дополнительными параметрами и сохраняет различия в предоставленный выходной поток в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Оригинальный документ. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Изменённый документ. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) опции сравнения. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), будет сохранена только первая страница вывода в указанный поток.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF в указанный поток.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::String\& | Оригинальный документ. |
| v2 | const System::String\& | Изменённый документ. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::String\& | Оригинальный документ. |
| v2 | const System::String\& | Изменённый документ. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) опции сравнения. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::String\& | Оригинальный документ. |
| v2 | const System::String\& | Изменённый документ. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::String\& | Оригинальный документ. |
| v2 | const System::String\& | Изменённый документ. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) опции сравнения. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) method


Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл, создавая изменения в виде ряда правок и форматных ревизий.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::String\& | Оригинальный документ. |
| v2 | const System::String\& | Изменённый документ. |
| outputFileName | const System::String\& | Имя выходного файла. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл, создавая изменения в виде ряда правок и форматных ревизий.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::String\& | Оригинальный документ. |
| v2 | const System::String\& | Изменённый документ. |
| outputFileName | const System::String\& | Имя выходного файла. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) опции сравнения. |
## Примечания


Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена как отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён как один многостраничный TIFF‑файл.

## См. также

* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
