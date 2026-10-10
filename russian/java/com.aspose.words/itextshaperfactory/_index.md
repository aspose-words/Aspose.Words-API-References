---
title: "ITextShaperFactory"
linktitle: "ITextShaperFactory"
second_title: "Aspose.Words для Java"
description: "Интерфейс фабрики для создания реализаций ITextShaper в Java."
type: docs
weight: 787
url: /ru/java/com.aspose.words/itextshaperfactory/
---
```
public interface ITextShaperFactory
```

Интерфейс фабрики для создания реализаций [ITextShaper](../../com.aspose.words/itextshaper/) .
## Методы

| Метод | Описание |
| --- | --- |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) | Возвращает новый экземпляр text shaper для шрифта, представленного  fontBlob  и  faceIndex . |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) | Возвращает новый экземпляр text shaper для шрифта, указанного  fontPath  и  faceIndex . |
### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public abstract ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Возвращает новый экземпляр text shaper для шрифта, представленного  fontBlob  и  faceIndex .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontId | java.lang.String | Уникальный идентификатор, который может быть однозначно связан с предоставленным шрифтом fontBlob . |
| fontBlob | byte[] | Массив байтов с данными шрифта. |
| faceIndex | int | Индекс начертания шрифта в коллекции TrueType, или 0, если  fontBlob  не является коллекцией TrueType. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int}
```
public abstract ITextShaper getTextShaper(String fontPath, int faceIndex)
```


Возвращает новый экземпляр text shaper для шрифта, указанного  fontPath  и  faceIndex .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontPath | java.lang.String | Абсолютный путь к файлу шрифта. |
| faceIndex | int | Индекс начертания шрифта в коллекции TrueType, или 0, если указанный файл шрифта не является коллекцией TrueType. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
