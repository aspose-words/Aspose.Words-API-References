---
title: IResourceSavingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет изображения, шрифты и css из внешних ресурсов при сохранении документа на фиксированную страницу HTML или SVG.
type: docs
weight: 657
url: /ru/java/com.aspose.words/iresourcesavingcallback/
---
```
public interface IResourceSavingCallback
```

Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет внешние ресурсы (изображения, шрифты и css) при сохранении документа на фиксированную страницу HTML или SVG.
## Методы

| Метод | Описание |
| --- | --- |
| [resourceSaving(ResourceSavingArgs args)](#resourceSaving-com.aspose.words.ResourceSavingArgs-) | Вызывается, когда Aspose.Words сохраняет внешний ресурс в формате фиксированной страницы HTML или SVG. |
### resourceSaving(ResourceSavingArgs args) {#resourceSaving-com.aspose.words.ResourceSavingArgs-}
```
public abstract void resourceSaving(ResourceSavingArgs args)
```


Вызывается, когда Aspose.Words сохраняет внешний ресурс в формате фиксированной страницы HTML или SVG.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [ResourceSavingArgs](../../com.aspose.words/resourcesavingargs) |  |
