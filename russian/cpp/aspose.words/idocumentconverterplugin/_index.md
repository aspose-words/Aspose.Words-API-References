---
title: "Интерфейс Aspose::Words::IDocumentConverterPlugin"
linktitle: "IDocumentConverterPlugin"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::IDocumentConverterPlugin. Определяет интерфейс для внешнего плагина конвертера на C++."
type: docs
weight: 76250
url: /ru/cpp/aspose.words/idocumentconverterplugin/
---
## IDocumentConverterPlugin interface


Определяет интерфейс для внешнего плагина конвертера.

```cpp
class IDocumentConverterPlugin : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [Convert](./convert/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Преобразует документ, используя указанные входные и выходные потоки и параметры сохранения. |
| virtual [ConvertToImages](./converttoimages/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Преобразует страницы документа из входного потока в массив изображений. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
