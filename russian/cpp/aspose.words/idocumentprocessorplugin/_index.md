---
title: "Интерфейс Aspose::Words::IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::IDocumentProcessorPlugin. Определяет интерфейс для внешнего плагина процессора документов на C++."
type: docs
weight: 76750
url: /ru/cpp/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface


Определяет интерфейс для внешнего плагина обработки документов.

```cpp
class IDocumentProcessorPlugin : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [Append](./append/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Добавьте документ, загрузив его с указанными параметрами загрузки. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Load](./load/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Загрузите документ, используя указанные параметры загрузки. |
| virtual [Save](./save/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Сохраните документ, загруженный методом [Load()](./load/), в выходной поток, используя указанные параметры сохранения. |
| virtual [SetImageWatermark](./setimagewatermark/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>) | Добавляет изображенный водяной знак на каждую страницу документа, загруженного методом [Load()](./load/). |
| virtual [SetTextWatermark](./settextwatermark/)(System::String, System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>) | Добавляет текстовый водяной знак на каждую страницу документа, загруженного методом [Load()](./load/). |
| virtual [ToDocument](./todocument/)() | Разбирает документ, загруженный методом [Load()](./load/), в объект [Document](../document/). |
| virtual [ToPages](./topages/)(System::SharedPtr\<Aspose::Words::Saving::FixedPageSaveOptions\>) | Сохраняет каждую страницу документа, загруженного методом [Load()](./load/), используя указанные параметры фиксированного сохранения страниц. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
