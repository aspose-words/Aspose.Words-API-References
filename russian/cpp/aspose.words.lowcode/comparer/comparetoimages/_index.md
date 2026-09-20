---
title: "Aspose::Words::LowCode::Comparer::CompareToImages метод"
linktitle: "CompareToImages"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Comparer::CompareToImages метод. Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент возвращаемого массива представляет отдельную страницу вывода, отрисованную как изображение в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.lowcode/comparer/comparetoimages/
---
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент возвращаемого массива представляет отдельную страницу вывода, отрисованную как изображение.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Оригинальный документ. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Изменённый документ. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения изображения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент возвращаемого массива представляет отдельную страницу вывода, отрисованную как изображение.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Оригинальный документ. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Изменённый документ. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения изображения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) опции сравнения. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент возвращаемого массива представляет отдельную страницу вывода, отрисованную как изображение.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::String\& | Оригинальный документ. |
| v2 | const System::String\& | Изменённый документ. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения изображения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент возвращаемого массива представляет отдельную страницу вывода, отрисованную как изображение.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| v1 | const System::String\& | Оригинальный документ. |
| v2 | const System::String\& | Изменённый документ. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения изображения вывода. |
| автор | const System::String\& | Инициалы автора, используемые для ревизий. |
| dateTime | System::DateTime | Дата и время, используемые для правок. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) опции сравнения. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
