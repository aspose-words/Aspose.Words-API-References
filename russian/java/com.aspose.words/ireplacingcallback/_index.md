---
title: IReplacingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если вы хотите, чтобы во время операции поиска и замены вызывался ваш собственный метод.
type: docs
weight: 655
url: /ru/java/com.aspose.words/ireplacingcallback/
---
```
public interface IReplacingCallback
```

Реализуйте этот интерфейс, если вы хотите, чтобы во время операции поиска и замены вызывался ваш собственный метод.
## Методы

| Метод | Описание |
| --- | --- |
| [replacing(ReplacingArgs args)](#replacing-com.aspose.words.ReplacingArgs-) | Определяемый пользователем метод, который вызывается во время операции замены для каждого совпадения, найденного непосредственно перед выполнением замены. |
### replacing(ReplacingArgs args) {#replacing-com.aspose.words.ReplacingArgs-}
```
public abstract int replacing(ReplacingArgs args)
```


Определяемый пользователем метод, который вызывается во время операции замены для каждого совпадения, найденного непосредственно перед выполнением замены.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [ReplacingArgs](../../com.aspose.words/replacingargs) |  |

**Возвращает:**
 интервал - А[ReplaceAction](../../com.aspose.words/replaceaction)значение, указывающее действие, которое необходимо выполнить для текущего совпадения. Возвращаемое значение является одним из[ReplaceAction](../../com.aspose.words/replaceaction) константы.