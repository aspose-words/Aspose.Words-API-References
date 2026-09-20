---
title: "Aspose::Words::Layout::PageLayoutCallbackArgs class"
linktitle: "PageLayoutCallbackArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Kласс Aspose::Words::Layout::PageLayoutCallbackArgs. Аргумент, передаваемый в Notify(). Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class


Аргумент, передаваемый в [Notify()](../ipagelayoutcallback/notify/). Чтобы узнать больше, посетите статью документации [Преобразование в фиксированный формат страниц](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class PageLayoutCallbackArgs : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Document](./get_document/)() const | Получает документ. |
| [get_Event](./get_event/)() const | Получает событие. |
| [get_PageIndex](./get_pageindex/)() | Получает нулевой индекс страницы в документе, к которой относится это событие. Возвращает отрицательное значение, если нет связанной страницы или если страница была удалена во время перерасчёта. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
