---
title: "BasicTextShaperCache"
linktitle: "BasicTextShaperCache"
second_title: "Aspose.Words для Java"
description: "Реализует базовый кэш для экземпляров ITextShaper в Java."
type: docs
weight: 37
url: /ru/java/com.aspose.words/basictextshapercache/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.ITextShaperFactory](../../com.aspose.words/itextshaperfactory/)
```
public class BasicTextShaperCache implements ITextShaperFactory
```

Реализует базовый кэш для экземпляров [ITextShaper](../../com.aspose.words/itextshaper/) . Этот класс потокобезопасен.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [BasicTextShaperCache(ITextShaperFactory factory)](#BasicTextShaperCache-com.aspose.words.ITextShaperFactory) | Оборачивает фабрику и кэширует результаты [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int). |
## Методы

| Метод | Описание |
| --- | --- |
| [dispose()](#dispose) | Освобождает кэшированные экземпляры [ITextShaper](../../com.aspose.words/itextshaper/). |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) |  |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) |  |
### BasicTextShaperCache(ITextShaperFactory factory) {#BasicTextShaperCache-com.aspose.words.ITextShaperFactory}
```
public BasicTextShaperCache(ITextShaperFactory factory)
```


Оборачивает фабрику и кэширует результаты [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| factory | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) |  |

### dispose() {#dispose}
```
public void dispose()
```


Освобождает кэшированные экземпляры [ITextShaper](../../com.aspose.words/itextshaper/).

### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Возвращает новый экземпляр text shaper для шрифта, представленного  fontBlob  и  faceIndex .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontId | java.lang.String |  |
| fontBlob | byte[] |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int}
```
public ITextShaper getTextShaper(String fontPath, int faceIndex)
```


Возвращает новый экземпляр text shaper для шрифта, указанного  fontPath  и  faceIndex .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fontPath | java.lang.String |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
