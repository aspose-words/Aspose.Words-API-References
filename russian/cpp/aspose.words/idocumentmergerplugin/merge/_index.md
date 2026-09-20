---
title: "Aspose::Words::IDocumentMergerPlugin::Merge метод"
linktitle: "Объединить"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::IDocumentMergerPlugin::Merge метод. Объединяет указанные входные PDF‑документы в один выходной PDF‑документ, используя указанные входные и выходные потоки в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/idocumentmergerplugin/merge/
---
## IDocumentMergerPlugin::Merge method


Объединяет указанные входные PDF‑документы в один выходной PDF‑документ, используя заданные входные и выходные потоки.

```cpp
virtual void Aspose::Words::IDocumentMergerPlugin::Merge(System::SharedPtr<System::IO::Stream> outputStream, System::ArrayPtr<System::SharedPtr<System::IO::Stream>> inputStreams, System::ArrayPtr<System::SharedPtr<Aspose::Words::Loading::LoadOptions>> loadOptions)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| outputStream | System::SharedPtr\<System::IO::Stream\> | Выходной поток. |
| inputStreams | System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\> | Входные потоки. |
| loadOptions | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\> | Параметры загрузки для входных файлов. |

## См. также

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Interface [IDocumentMergerPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
