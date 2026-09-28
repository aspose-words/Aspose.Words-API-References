---
title: "Интерфейс Aspose::Words::Saving::IImageSavingCallback"
linktitle: "IImageSavingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::Saving::IImageSavingCallback. Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет изображения при сохранении документа в HTML. Может использоваться другими форматами в C++."
type: docs
weight: 43000
url: /ru/cpp/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface


Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет изображения при сохранении документа в HTML. Может использоваться другими форматами.

```cpp
class IImageSavingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| virtual [ImageSaving](./imagesaving/)(System::SharedPtr\<Aspose::Words::Saving::ImageSavingArgs\>) | Вызывается, когда Aspose.Words сохраняет изображение в HTML. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
