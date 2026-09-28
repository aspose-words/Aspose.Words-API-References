---
title: "Aspose::Words::Saving::ICssSavingCallback интерфейс"
linktitle: "ICssSavingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ICssSavingCallback интерфейс. Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет CSS (Cascading Style Sheet) при сохранении документа в HTML в C++."
type: docs
weight: 39000
url: /ru/cpp/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface


Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет CSS (Cascading [Style](../../aspose.words/style/) Sheet) при сохранении документа в HTML.

```cpp
class ICssSavingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [CssSaving](./csssaving/)(System::SharedPtr\<Aspose::Words::Saving::CssSavingArgs\>) | Вызывается, когда Aspose.Words сохраняет CSS (каскадный [Style](../../aspose.words/style/) лист). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
