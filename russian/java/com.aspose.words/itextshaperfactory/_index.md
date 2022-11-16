---
title: ITextShaperFactory
second_title: Справочник по API Aspose.Words для Java
description: 
type: docs
weight: 660
url: /ru/java/com.aspose.words/itextshaperfactory/
---
```
public interface ITextShaperFactory
```
## Методы

| Метод | Описание |
| --- | --- |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int-) |  |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int-) |  |
### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int-}
```
public abstract ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontId | java.lang.String |  |
| fontBlob | byte[] |  |
| faceIndex | int |  |

**Возвращает:**
[ITextShaper](../../com.aspose.words/itextshaper)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int-}
```
public abstract ITextShaper getTextShaper(String fontPath, int faceIndex)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontPath | java.lang.String |  |
| faceIndex | int |  |

**Возвращает:**
[ITextShaper](../../com.aspose.words/itextshaper)