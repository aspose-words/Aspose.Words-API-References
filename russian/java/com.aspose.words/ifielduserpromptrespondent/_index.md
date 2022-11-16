---
title: IFieldUserPromptRespondent
second_title: Справочник по API Aspose.Words для Java
description: Представляет ответчика на запросы пользователя во время обновления поля.
type: docs
weight: 645
url: /ru/java/com.aspose.words/ifielduserpromptrespondent/
---
```
public interface IFieldUserPromptRespondent
```

Представляет ответчика на запросы пользователя во время обновления поля. Поля ASK и FILLIN являются примерами полей, которые запрашивают у пользователя некоторый ответ. Реализуйте этот интерфейс и назначьте его[FieldOptions.getUserPromptRespondent()](../../com.aspose.words/fieldoptions\#getUserPromptRespondent--) / [FieldOptions.setUserPromptRespondent(com.aspose.words.IFieldUserPromptRespondent)](../../com.aspose.words/fieldoptions\#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent-) свойство для установления взаимодействия между обновлением поля и пользователем.
## Методы

| Метод | Описание |
| --- | --- |
| [respond(String promptText, String defaultResponse)](#respond-java.lang.String-java.lang.String-) | При реализации возвращает ответ пользователя на запрос. |
### respond(String promptText, String defaultResponse) {#respond-java.lang.String-java.lang.String-}
```
public abstract String respond(String promptText, String defaultResponse)
```


 При реализации возвращает ответ пользователя на запрос. Ваша реализация должна вернуться**null** чтобы указать, что пользователь не ответил на подсказку (т. е. пользователь нажал кнопку «Отмена» в окне подсказки).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| promptText | java.lang.String | Текст подсказки (т.е. заголовок окна подсказки). |
| defaultResponse | java.lang.String | Ответ пользователя по умолчанию (т. е. начальное значение, содержащееся в окне подсказки). |

**Возвращает:**
java.lang.String — ответ пользователя (т. е. подтвержденное значение, содержащееся в окне подсказки).