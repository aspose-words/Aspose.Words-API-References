---
title: "BasicTextShaperCache"
linktitle: "BasicTextShaperCache"
second_title: "Aspose.Words für Java"
description: "Implementiert einen einfachen Cache für ITextShaper‑Instanzen in Java."
type: docs
weight: 37
url: /de/java/com.aspose.words/basictextshapercache/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.ITextShaperFactory](../../com.aspose.words/itextshaperfactory/)
```
public class BasicTextShaperCache implements ITextShaperFactory
```

Implementiert einen einfachen Cache für [ITextShaper](../../com.aspose.words/itextshaper/)‑Instanzen. Diese Klasse ist thread‑sicher.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [BasicTextShaperCache(ITextShaperFactory factory)](#BasicTextShaperCache-com.aspose.words.ITextShaperFactory) | Umwickelt die Factory und cached die Ergebnisse von [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int). |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [dispose()](#dispose) | Gibt zwischengespeicherte [ITextShaper](../../com.aspose.words/itextshaper/)‑Instanzen frei. |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) |  |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) |  |
### BasicTextShaperCache(ITextShaperFactory factory) {#BasicTextShaperCache-com.aspose.words.ITextShaperFactory}
```
public BasicTextShaperCache(ITextShaperFactory factory)
```


Umwickelt die Factory und cached die Ergebnisse von [ITextShaperFactory.getTextShaper(java.lang.String, int)](../../com.aspose.words/itextshaperfactory/\#getTextShaper-java.lang.String--int).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| factory | [ITextShaperFactory](../../com.aspose.words/itextshaperfactory/) |  |

### dispose() {#dispose}
```
public void dispose()
```


Gibt zwischengespeicherte [ITextShaper](../../com.aspose.words/itextshaper/)‑Instanzen frei.

### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Gibt eine neue Instanz eines Text‑Shapers für die Schrift zurück, die durch  fontBlob  und  faceIndex  dargestellt wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
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


Gibt eine neue Instanz eines Text‑Shapers für die Schrift zurück, die durch  fontPath  und  faceIndex  angegeben ist.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontPath | java.lang.String |  |
| faceIndex | int |  |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
