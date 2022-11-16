---
title: IFontSavingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если хотите получать уведомления и управлять тем, как Aspose.Words сохраняет шрифты при экспорте документа в формат HTML.
type: docs
weight: 646
url: /ru/java/com.aspose.words/ifontsavingcallback/
---
```
public interface IFontSavingCallback
```

Реализуйте этот интерфейс, если хотите получать уведомления и управлять тем, как Aspose.Words сохраняет шрифты при экспорте документа в формат HTML.
## Методы

| Метод | Описание |
| --- | --- |
| [fontSaving(FontSavingArgs args)](#fontSaving-com.aspose.words.FontSavingArgs-) | Вызывается, когда Aspose.Words собирается сохранить ресурс шрифта. |
### fontSaving(FontSavingArgs args) {#fontSaving-com.aspose.words.FontSavingArgs-}
```
public abstract void fontSaving(FontSavingArgs args)
```


Вызывается, когда Aspose.Words собирается сохранить ресурс шрифта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [FontSavingArgs](../../com.aspose.words/fontsavingargs) |  |
