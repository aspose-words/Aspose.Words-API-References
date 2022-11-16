---
title: IFieldMergingCallback
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, если вы хотите контролировать, как данные вставляются в поля слияния во время операции слияния.
type: docs
weight: 641
url: /ru/java/com.aspose.words/ifieldmergingcallback/
---
```
public interface IFieldMergingCallback
```

Реализуйте этот интерфейс, если вы хотите контролировать, как данные вставляются в поля слияния во время операции слияния.
## Методы

| Метод | Описание |
| --- | --- |
| [fieldMerging(FieldMergingArgs args)](#fieldMerging-com.aspose.words.FieldMergingArgs-) | Вызывается, когда механизм слияния Aspose.Words собирается вставить данные в поле слияния в документе. |
| [imageFieldMerging(ImageFieldMergingArgs args)](#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs-) | Вызывается, когда механизм слияния Aspose.Words собирается вставить изображение в поле слияния. |
### fieldMerging(FieldMergingArgs args) {#fieldMerging-com.aspose.words.FieldMergingArgs-}
```
public abstract void fieldMerging(FieldMergingArgs args)
```


Вызывается, когда механизм слияния Aspose.Words собирается вставить данные в поле слияния в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [FieldMergingArgs](../../com.aspose.words/fieldmergingargs) |  |

### imageFieldMerging(ImageFieldMergingArgs args) {#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs-}
```
public abstract void imageFieldMerging(ImageFieldMergingArgs args)
```


Вызывается, когда механизм слияния Aspose.Words собирается вставить изображение в поле слияния.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [ImageFieldMergingArgs](../../com.aspose.words/imagefieldmergingargs) |  |
