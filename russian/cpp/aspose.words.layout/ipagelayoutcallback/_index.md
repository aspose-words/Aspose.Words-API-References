---
title: "Aspose::Words::Layout::IPageLayoutCallback интерфейс"
linktitle: "IPageLayoutCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::IPageLayoutCallback интерфейс. Реализуйте этот интерфейс, если вы хотите иметь собственный пользовательский метод, вызываемый во время построения и рендеринга модели разметки страницы в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface


Реализуйте этот интерфейс, если хотите иметь собственный пользовательский метод, вызываемый во время построения и отрисовки модели компоновки страниц.

```cpp
class IPageLayoutCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Layout::PageLayoutCallbackArgs\>) | Это вызывается для уведомления о прогрессе построения и рендеринга разметки. |
| static [Type](./type/)() |  |
## Примечания


Основное назначение этого интерфейса — позволить коду приложения прервать процесс построения.

Можно построить модель разметки страницы только для нескольких страниц в начале документа, затем прервать процесс и отрендерить только то, что уже построено.

Однако обратите внимание, что результаты рендеринга могут не соответствовать тому, что было бы отрендерено для каждой страницы, если процесс завершился бы.

Эта техника может не работать для каждого документа или может полностью провалиться.

## См. также

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
