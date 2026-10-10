---
title: "BasicTextShaperCache"
linktitle: "BasicTextShaperCache"
second_title: "Aspose.Words para Java"
description: "Implementa una caché básica para instancias de ITextShaper en Java."
type: docs
weight: 37
url: /es/java/com.aspose.words/basictextshapercache/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.ITextShaperFactory](../../com.aspose.words/itextshaperfactory/)
```
public class BasicTextShaperCache implements ITextShaperFactory
```

Implementa una caché básica para instancias de [ITextShaper](../../com.aspose.words/itextshaper/). Esta clase es segura para subprocesos.
## Constructores

| Constructor | Descripción |
| --- | --- |
| [BasicTextShaperCache(ITextShaperFactory factory)](#BasicTextShaperCache-com.aspose.words.ITextShaperFactory) | Envuelve la fábrica y almacena en caché los resultados de [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\\#getTextShaper-java.lang.String--int). |
## Métodos

| Método | Descripción |
| --- | --- |
| [dispose()](#dispose) | Elimina las instancias en caché de [ITextShaper](../../com.aspose.words/itextshaper/). |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) |  |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) |  |
### BasicTextShaperCache(ITextShaperFactory factory) {#BasicTextShaperCache-com.aspose.words.ITextShaperFactory}
```
public BasicTextShaperCache(ITextShaperFactory factory)
```


Envuelve la fábrica y almacena en caché los resultados de [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\\#getTextShaper-java.lang.String--int).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| factory | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) |  |

### dispose() {#dispose}
```
public void dispose()
```


Elimina las instancias en caché de [ITextShaper](../../com.aspose.words/itextshaper/).

### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Devuelve una nueva instancia de un text shaper para la fuente representada por  fontBlob  y  faceIndex .

**Parameters:**
| Parámetro | Tipo | Descripción |
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


Devuelve una nueva instancia de un text shaper para la fuente especificada por  fontPath  y  faceIndex .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontPath | java.lang.String |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
