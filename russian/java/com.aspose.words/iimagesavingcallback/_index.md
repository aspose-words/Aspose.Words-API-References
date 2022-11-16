---
title: IImageSavingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет изображения при сохранении документа в HTML.
type: docs
weight: 648
url: /ru/java/com.aspose.words/iimagesavingcallback/
---
```
public interface IImageSavingCallback
```

Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет изображения при сохранении документа в HTML. Может использоваться другими форматами.
## Методы

| Метод | Описание |
| --- | --- |
| [imageSaving(ImageSavingArgs args)](#imageSaving-com.aspose.words.ImageSavingArgs-) | Вызывается, когда Aspose.Words сохраняет изображение в HTML. |
### imageSaving(ImageSavingArgs args) {#imageSaving-com.aspose.words.ImageSavingArgs-}
```
public abstract void imageSaving(ImageSavingArgs args)
```


Вызывается, когда Aspose.Words сохраняет изображение в HTML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [ImageSavingArgs](../../com.aspose.words/imagesavingargs) |  |
