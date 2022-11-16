---
title: IFieldUpdatingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если вы хотите, чтобы во время обновления поля вызывались ваши собственные пользовательские методы.
type: docs
weight: 644
url: /ru/java/com.aspose.words/ifieldupdatingcallback/
---
```
public interface IFieldUpdatingCallback
```

Реализуйте этот интерфейс, если вы хотите, чтобы во время обновления поля вызывались ваши собственные пользовательские методы.
## Методы

| Метод | Описание |
| --- | --- |
| [fieldUpdated(Field field)](#fieldUpdated-com.aspose.words.Field-) | Определяемый пользователем метод, который вызывается сразу после обновления поля. |
| [fieldUpdating(Field field)](#fieldUpdating-com.aspose.words.Field-) | Определенный пользователем метод, который вызывается непосредственно перед обновлением поля. |
### fieldUpdated(Field field) {#fieldUpdated-com.aspose.words.Field-}
```
public abstract void fieldUpdated(Field field)
```


Определяемый пользователем метод, который вызывается сразу после обновления поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) |  |

### fieldUpdating(Field field) {#fieldUpdating-com.aspose.words.Field-}
```
public abstract void fieldUpdating(Field field)
```


Определенный пользователем метод, который вызывается непосредственно перед обновлением поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) |  |
