---
title: "интерфейс Aspose::Words::Saving::IFontSavingCallback"
linktitle: "IFontSavingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::Saving::IFontSavingCallback. Реализуйте этот интерфейс, если хотите получать уведомления и контролировать, как Aspose.Words сохраняет шрифты при экспорте документа в формат HTML на C++."
type: docs
weight: 42000
url: /ru/cpp/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface


Реализуйте этот интерфейс, если вы хотите получать уведомления и контролировать, как Aspose.Words сохраняет шрифты при экспорте документа в формат HTML.

```cpp
class IFontSavingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [FontSaving](./fontsaving/)(System::SharedPtr\<Aspose::Words::Saving::FontSavingArgs\>) | Вызывается, когда Aspose.Words собирается сохранить ресурс шрифта. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
