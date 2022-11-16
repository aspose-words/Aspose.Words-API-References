---
title: IResourceLoadingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words загружает внешний ресурс при импорте документа и вставке изображений с использованием файлов .
type: docs
weight: 656
url: /ru/java/com.aspose.words/iresourceloadingcallback/
---
```
public interface IResourceLoadingCallback
```

 Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words загружает внешний ресурс при импорте документа и вставке изображений с помощью[DocumentBuilder](../../com.aspose.words/documentbuilder).
## Методы

| Метод | Описание |
| --- | --- |
| [resourceLoading(ResourceLoadingArgs args)](#resourceLoading-com.aspose.words.ResourceLoadingArgs-) | Вызывается, когда Aspose.Words загружает любой внешний ресурс. |
### resourceLoading(ResourceLoadingArgs args) {#resourceLoading-com.aspose.words.ResourceLoadingArgs-}
```
public abstract int resourceLoading(ResourceLoadingArgs args)
```


Вызывается, когда Aspose.Words загружает любой внешний ресурс.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [ResourceLoadingArgs](../../com.aspose.words/resourceloadingargs) |  |

**Возвращает:**
инт