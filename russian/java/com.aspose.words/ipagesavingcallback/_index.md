---
title: IPageSavingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет отдельные страницы при сохранении документа в фиксированных форматах страниц.
type: docs
weight: 654
url: /ru/java/com.aspose.words/ipagesavingcallback/
---
```
public interface IPageSavingCallback
```

Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет отдельные страницы при сохранении документа в фиксированных форматах страниц.
## Методы

| Метод | Описание |
| --- | --- |
| [pageSaving(PageSavingArgs args)](#pageSaving-com.aspose.words.PageSavingArgs-) | Вызывается, когда Aspose.Words сохраняет отдельную страницу в фиксированных форматах страниц. |
### pageSaving(PageSavingArgs args) {#pageSaving-com.aspose.words.PageSavingArgs-}
```
public abstract void pageSaving(PageSavingArgs args)
```


Вызывается, когда Aspose.Words сохраняет отдельную страницу в фиксированных форматах страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [PageSavingArgs](../../com.aspose.words/pagesavingargs) |  |
