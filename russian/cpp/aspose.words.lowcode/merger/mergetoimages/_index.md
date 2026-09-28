---
title: "Aspose::Words::LowCode::Merger::MergeToImages метод"
linktitle: "MergeToImages"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Merger::MergeToImages метод. Объединяет указанные входные потоки документов в один выходной документ, используя указанные параметры сохранения изображения. Рендерит вывод в изображения в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.lowcode/merger/mergetoimages/
---
## Merger::MergeToImages(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Объединяет указанные потоки входных документов в один выходной документ, используя заданные параметры сохранения изображений. Отображает вывод в виде изображений.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | Входные файловые потоки. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Указывает, как объединять конфликтующее форматирование. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::MergeToImages(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Объединяет указанные входные документы в один выходной документ, используя заданные имена входного и выходного файлов и параметры сохранения. Отображает вывод в виде изображений.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::String> &inputFiles, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFiles | const System::ArrayPtr\<System::String\>\& | Имена входных файлов. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Параметры сохранения. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Указывает, как объединять конфликтующее форматирование. |

## См. также

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
