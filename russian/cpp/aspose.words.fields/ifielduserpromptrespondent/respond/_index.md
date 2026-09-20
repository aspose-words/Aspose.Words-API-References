---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond метод"
linktitle: "Respond"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond метод. При реализации возвращает ответ пользователя на запрос. Ваша реализация должна возвращать null, чтобы указать, что пользователь не ответил на запрос (т. е. пользователь нажал кнопку Отмена в окне подсказки) в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent::Respond method


При реализации возвращает ответ пользователя на запрос. Ваша реализация должна возвращать **null**, чтобы указать, что пользователь не ответил на запрос (т. е. пользователь нажал кнопку Отмена в окне запроса).

```cpp
virtual System::String Aspose::Words::Fields::IFieldUserPromptRespondent::Respond(System::String promptText, System::String defaultResponse)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| promptText | System::String | Текст подсказки (т. е. заголовок окна подсказки). |
| defaultResponse | System::String | Ответ пользователя по умолчанию (т. е. начальное значение, содержащееся в окне подсказки). |

### ReturnValue

Ответ пользователя (т. е. подтверждённое значение, содержащееся в окне подсказки).

## См. также

* Interface [IFieldUserPromptRespondent](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
