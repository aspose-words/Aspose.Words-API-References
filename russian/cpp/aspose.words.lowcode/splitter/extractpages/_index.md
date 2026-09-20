---
title: "Метод Aspose::Words::LowCode::Splitter::ExtractPages"
linktitle: "ExtractPages"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::LowCode::Splitter::ExtractPages. Извлекает указанный диапазон страниц из потока документа и сохраняет извлечённые страницы в выходной поток с использованием указанного формата сохранения в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.lowcode/splitter/extractpages/
---
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Извлекает указанный диапазон страниц из потока документа и сохраняет извлечённые страницы в выходной поток, используя указанный формат сохранения.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| startPageIndex | int32_t | Нулевой индекс первой страницы для извлечения. |
| pageCount | int32_t | Количество страниц для извлечения. |

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Извлекает указанный диапазон страниц из потока документа и сохраняет извлечённые страницы в выходной поток, используя указанный формат сохранения.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Входной поток. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Выходной поток. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| startPageIndex | int32_t | Нулевой индекс первой страницы для извлечения. |
| pageCount | int32_t | Количество страниц для извлечения. |

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Извлекает указанный диапазон страниц из файла документа и сохраняет извлечённые страницы в новый файл, используя указанный формат сохранения.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveFormat | Aspose::Words::SaveFormat | Формат сохранения. |
| startPageIndex | int32_t | Нулевой индекс первой страницы для извлечения. |
| pageCount | int32_t | Количество страниц для извлечения. |

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Извлекает указанный диапазон страниц из файла документа и сохраняет извлечённые страницы в новый файл, используя указанный формат сохранения.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Параметры сохранения. |
| startPageIndex | int32_t | Нулевой индекс первой страницы для извлечения. |
| pageCount | int32_t | Количество страниц для извлечения. |

## См. также

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, int32_t, int32_t) method


Извлекает указанный диапазон страниц из файла документа и сохраняет извлечённые страницы в новый файл. Формат выходного файла определяется расширением имени выходного файла.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, int32_t startPageIndex, int32_t pageCount)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | const System::String\& | Имя входного файла. |
| outputFileName | const System::String\& | Имя выходного файла. |
| startPageIndex | int32_t | Нулевой индекс первой страницы для извлечения. |
| pageCount | int32_t | Количество страниц для извлечения. |

## См. также

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
