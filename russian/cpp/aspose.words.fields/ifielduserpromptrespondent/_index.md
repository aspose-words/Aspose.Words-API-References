---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent interface"
linktitle: "IFieldUserPromptRespondent"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent interface. Представляет ответчика на запросы пользователя во время обновления поля в C++."
type: docs
weight: 125000
url: /ru/cpp/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface


Представляет ответчика на запросы пользователя во время обновления поля.

```cpp
class IFieldUserPromptRespondent : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Respond](./respond/)(System::String, System::String) | При реализации возвращает ответ пользователя на запрос. Ваша реализация должна возвращать **null**, чтобы указать, что пользователь не ответил на запрос (т. е. пользователь нажал кнопку Отмена в окне запроса). |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
