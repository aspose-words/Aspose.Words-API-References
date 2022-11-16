---
title: IDocumentSavingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если вы хотите, чтобы во время сохранения документа вызывался ваш собственный метод.
type: docs
weight: 639
url: /ru/java/com.aspose.words/idocumentsavingcallback/
---
```
public interface IDocumentSavingCallback
```

Реализуйте этот интерфейс, если вы хотите, чтобы во время сохранения документа вызывался ваш собственный метод.
## Методы

| Метод | Описание |
| --- | --- |
| [notify(DocumentSavingArgs args)](#notify-com.aspose.words.DocumentSavingArgs-) | Это вызывается для уведомления о ходе сохранения документа. |
### notify(DocumentSavingArgs args) {#notify-com.aspose.words.DocumentSavingArgs-}
```
public abstract void notify(DocumentSavingArgs args)
```


Это вызывается для уведомления о ходе сохранения документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [DocumentSavingArgs](../../com.aspose.words/documentsavingargs) | Аргумент события. Основное использование этого интерфейса — разрешить коду приложения получать статус выполнения и прерывать процесс сохранения.

 Исключение должно быть выброшено из обратного вызова прогресса для аборта и должно быть перехвачено в коде потребителя.|
