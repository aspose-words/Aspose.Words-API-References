---
title: "Интерфейс Aspose::Words::IDocumentMergerPlugin"
linktitle: "IDocumentMergerPlugin"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::IDocumentMergerPlugin interface. Определяет интерфейс для внешнего плагина слияния, который может объединять PDF‑документы в C++."
type: docs
weight: 76500
url: /ru/cpp/aspose.words/idocumentmergerplugin/
---
## IDocumentMergerPlugin interface


Определяет интерфейс для внешнего плагина слияния, который может объединять PDF‑документы.

```cpp
class IDocumentMergerPlugin : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Merge](./merge/)(System::SharedPtr\<System::IO::Stream\>, System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>, System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>) | Объединяет указанные входные PDF‑документы в один выходной PDF‑документ, используя заданные входные и выходные потоки. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
