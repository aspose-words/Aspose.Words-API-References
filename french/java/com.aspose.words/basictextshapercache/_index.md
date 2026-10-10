---
title: "BasicTextShaperCache"
linktitle: "BasicTextShaperCache"
second_title: "Aspose.Words pour Java"
description: "Implémente un cache de base pour les instances ITextShaper en Java."
type: docs
weight: 37
url: /fr/java/com.aspose.words/basictextshapercache/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.ITextShaperFactory](../../com.aspose.words/itextshaperfactory/)
```
public class BasicTextShaperCache implements ITextShaperFactory
```

Implémente un cache de base pour les instances [ITextShaper](../../com.aspose.words/itextshaper/) . Cette classe est thread-safe.
## Constructors

| Constructor | Description |
| --- | --- |
| [BasicTextShaperCache(ITextShaperFactory factory)](#BasicTextShaperCache-com.aspose.words.ITextShaperFactory) | Enveloppe la factory et met en cache les résultats de [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int). |
## Méthodes

| Méthode | Description |
| --- | --- |
| [dispose()](#dispose) | Libère les instances [ITextShaper](../../com.aspose.words/itextshaper/) mises en cache. |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) |  |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) |  |
### BasicTextShaperCache(ITextShaperFactory factory) {#BasicTextShaperCache-com.aspose.words.ITextShaperFactory}
```
public BasicTextShaperCache(ITextShaperFactory factory)
```


Enveloppe la factory et met en cache les résultats de [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| factory | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) |  |

### dispose() {#dispose}
```
public void dispose()
```


Libère les instances [ITextShaper](../../com.aspose.words/itextshaper/) mises en cache.

### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Renvoie une nouvelle instance d'un text shaper pour la police représentée par  fontBlob  et  faceIndex .

**Parameters:**
| Paramètre | Type | Description |
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


Renvoie une nouvelle instance d'un text shaper pour la police spécifiée par  fontPath  et  faceIndex .

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fontPath | java.lang.String |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
