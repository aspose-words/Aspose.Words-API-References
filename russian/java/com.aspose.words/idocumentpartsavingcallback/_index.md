---
title: IDocumentPartSavingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если хотите получать уведомления и управлять тем, как Aspose.Words сохраняет части документа при экспорте документа в формат или формат.
type: docs
weight: 637
url: /ru/java/com.aspose.words/idocumentpartsavingcallback/
---
```
public interface IDocumentPartSavingCallback
```

 Реализуйте этот интерфейс, если хотите получать уведомления и управлять тем, как Aspose.Words сохраняет части документа при экспорте документа в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML) или же[SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) формат.
## Методы

| Метод | Описание |
| --- | --- |
| [documentPartSaving(DocumentPartSavingArgs args)](#documentPartSaving-com.aspose.words.DocumentPartSavingArgs-) | Вызывается, когда Aspose.Words собирается сохранить часть документа. |
### documentPartSaving(DocumentPartSavingArgs args) {#documentPartSaving-com.aspose.words.DocumentPartSavingArgs-}
```
public abstract void documentPartSaving(DocumentPartSavingArgs args)
```


Вызывается, когда Aspose.Words собирается сохранить часть документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [DocumentPartSavingArgs](../../com.aspose.words/documentpartsavingargs) |  |
