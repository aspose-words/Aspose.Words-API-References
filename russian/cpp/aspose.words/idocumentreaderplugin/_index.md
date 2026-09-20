---
title: "Aspose::Words::IDocumentReaderPlugin интерфейс"
linktitle: "IDocumentReaderPlugin"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::IDocumentReaderPlugin interface. Определяет интерфейс для внешних плагинов чтения, которые могут читать файл в документ в C++."
type: docs
weight: 77000
url: /ru/cpp/aspose.words/idocumentreaderplugin/
---
## IDocumentReaderPlugin interface


Определяет интерфейс для внешних плагинов‑чтения, которые могут читать файл в документ.

```cpp
class IDocumentReaderPlugin : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Read](./read/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Document\>) | Считывает данные из указанного потока в экземпляр [Document](../document/). |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
