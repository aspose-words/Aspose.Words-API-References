---
title: "Метод Aspose::Words::IDocumentConverterPlugin::Convert"
linktitle: "Конвертировать"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::IDocumentConverterPlugin::Convert method. Преобразует документ, используя указанные входные и выходные потоки и параметры сохранения в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/idocumentconverterplugin/convert/
---
## IDocumentConverterPlugin::Convert method


Преобразует документ, используя указанные входные и выходные потоки и параметры сохранения.

```cpp
virtual void Aspose::Words::IDocumentConverterPlugin::Convert(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<System::IO::Stream> outputStream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | Входной поток. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Параметры загрузки документа. |
| outputStream | System::SharedPtr\<System::IO::Stream\> | Выходной поток. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | Параметры сохранения. |

## См. также

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
