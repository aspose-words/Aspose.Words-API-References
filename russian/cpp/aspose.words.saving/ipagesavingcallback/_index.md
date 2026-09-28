---
title: "интерфейс Aspose::Words::Saving::IPageSavingCallback"
linktitle: "IPageSavingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "интерфейс Aspose::Words::Saving::IPageSavingCallback. Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет отдельные страницы при сохранении документа в фиксированные форматы страниц в C++."
type: docs
weight: 44000
url: /ru/cpp/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface


Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет отдельные страницы при сохранении документа в фиксированные форматы страниц.

```cpp
class IPageSavingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [PageSaving](./pagesaving/)(System::SharedPtr\<Aspose::Words::Saving::PageSavingArgs\>) | Вызывается, когда Aspose.Words сохраняет отдельную страницу в фиксированные форматы страниц. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
