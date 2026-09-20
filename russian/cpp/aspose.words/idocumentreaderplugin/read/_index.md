---
title: "Метод Aspose::Words::IDocumentReaderPlugin::Read"
linktitle: "Read"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::IDocumentReaderPlugin::Read. Считывает данные из указанного потока в экземпляр Document в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/idocumentreaderplugin/read/
---
## IDocumentReaderPlugin::Read method


Считывает данные из указанного потока в экземпляр [Document](../../document/).

```cpp
virtual void Aspose::Words::IDocumentReaderPlugin::Read(System::SharedPtr<System::IO::Stream> src, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Document> document)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| src | System::SharedPtr\<System::IO::Stream\> | Исходный поток, из которого считывается документ. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Дополнительные параметры загрузки для загрузки документа. |
| document | System::SharedPtr\<Aspose::Words::Document\> | Экземпляр класса [Document](../../document/), в который считываются данные. Если экземпляр уже содержит какое‑то содержимое, оно будет заменено данными из исходного потока. |

## См. также

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../../document/)
* Interface [IDocumentReaderPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
