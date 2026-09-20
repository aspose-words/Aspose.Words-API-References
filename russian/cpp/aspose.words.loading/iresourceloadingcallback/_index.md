---
title: "Aspose::Words::Loading::IResourceLoadingCallback интерфейс"
linktitle: "IResourceLoadingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::IResourceLoadingCallback интерфейс. Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words загружает внешние ресурсы при импорте документа и вставке изображений с помощью DocumentBuilder в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface


Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words загружает внешние ресурсы при вставке изображений с помощью [DocumentBuilder](../../aspose.words/documentbuilder/).

```cpp
class IResourceLoadingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceLoading](./resourceloading/)(System::SharedPtr\<Aspose::Words::Loading::ResourceLoadingArgs\>) | Вызывается, когда Aspose.Words загружает любой внешний ресурс. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
