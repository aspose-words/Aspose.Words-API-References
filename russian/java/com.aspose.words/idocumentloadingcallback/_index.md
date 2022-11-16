---
title: IDocumentLoadingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если вы хотите, чтобы во время загрузки документа вызывался ваш собственный метод.
type: docs
weight: 636
url: /ru/java/com.aspose.words/idocumentloadingcallback/
---
```
public interface IDocumentLoadingCallback
```

Реализуйте этот интерфейс, если вы хотите, чтобы во время загрузки документа вызывался ваш собственный метод.
## Методы

| Метод | Описание |
| --- | --- |
| [notify(DocumentLoadingArgs args)](#notify-com.aspose.words.DocumentLoadingArgs-) | Это вызывается для уведомления о ходе загрузки документа. |
### notify(DocumentLoadingArgs args) {#notify-com.aspose.words.DocumentLoadingArgs-}
```
public abstract void notify(DocumentLoadingArgs args)
```


Это вызывается для уведомления о ходе загрузки документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [DocumentLoadingArgs](../../com.aspose.words/documentloadingargs) | Аргумент события. Основное использование этого интерфейса — разрешить коду приложения получать статус выполнения и прерывать процесс загрузки.

 Исключение должно быть выброшено из обратного вызова прогресса для аборта и должно быть перехвачено в коде потребителя.|
