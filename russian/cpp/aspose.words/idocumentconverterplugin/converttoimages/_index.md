---
title: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages method"
linktitle: "ConvertToImages"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages method. Преобразует страницы документа из входного потока в массив изображений в C++."
type: docs
weight: 2500
url: /ru/cpp/aspose.words/idocumentconverterplugin/converttoimages/
---
## IDocumentConverterPlugin::ConvertToImages method


Преобразует страницы документа из входного потока в массив изображений.

```cpp
virtual System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::IDocumentConverterPlugin::ConvertToImages(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | Входной поток. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Параметры загрузки документа. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | Параметры сохранения. |

### ReturnValue

Массив потоков изображений страниц.

## См. также

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
