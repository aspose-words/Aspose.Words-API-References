---
title: "BasicTextShaperCache"
linktitle: "BasicTextShaperCache"
second_title: "Aspose.Words per Java"
description: "Implementa una cache di base per le istanze di ITextShaper in Java."
type: docs
weight: 37
url: /it/java/com.aspose.words/basictextshapercache/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.ITextShaperFactory](../../com.aspose.words/itextshaperfactory/)
```
public class BasicTextShaperCache implements ITextShaperFactory
```

Implementa una cache di base per le istanze di [ITextShaper](../../com.aspose.words/itextshaper/). Questa classe è thread-safe.
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [BasicTextShaperCache(ITextShaperFactory factory)](#BasicTextShaperCache-com.aspose.words.ITextShaperFactory) | Avvolge la factory e memorizza nella cache i risultati di [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int). |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [dispose()](#dispose) | Rilascia le istanze di [ITextShaper](../../com.aspose.words/itextshaper/) memorizzate nella cache. |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) |  |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) |  |
### BasicTextShaperCache(ITextShaperFactory factory) {#BasicTextShaperCache-com.aspose.words.ITextShaperFactory}
```
public BasicTextShaperCache(ITextShaperFactory factory)
```


Avvolge la factory e memorizza nella cache i risultati di [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| factory | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) |  |

### dispose() {#dispose}
```
public void dispose()
```


Rilascia le istanze di [ITextShaper](../../com.aspose.words/itextshaper/) memorizzate nella cache.

### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Restituisce una nuova istanza di un text shaper per il font rappresentato da  fontBlob  e  faceIndex .

**Parameters:**
| Parametro | Tipo | Descrizione |
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


Restituisce una nuova istanza di un text shaper per il font specificato da  fontPath  e  faceIndex .

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontPath | java.lang.String |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
