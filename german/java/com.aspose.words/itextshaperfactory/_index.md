---
title: "ITextShaperFactory"
linktitle: "ITextShaperFactory"
second_title: "Aspose.Words für Java"
description: "Eine Schnittstelle einer Fabrik zum Erzeugen von ITextShaper‑Implementierungen in Java."
type: docs
weight: 787
url: /de/java/com.aspose.words/itextshaperfactory/
---
```
public interface ITextShaperFactory
```

Eine Schnittstelle einer Fabrik zum Erzeugen von [ITextShaper](../../com.aspose.words/itextshaper/) Implementierungen.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) | Gibt eine neue Instanz eines Text‑Shapers für die Schrift zurück, die durch  fontBlob  und  faceIndex  dargestellt wird. |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) | Gibt eine neue Instanz eines Text‑Shapers für die Schrift zurück, die durch  fontPath  und  faceIndex  angegeben ist. |
### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public abstract ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Gibt eine neue Instanz eines Text‑Shapers für die Schrift zurück, die durch  fontBlob  und  faceIndex  dargestellt wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontId | java.lang.String | Ein eindeutiger Bezeichner, der eindeutig dem bereitgestellten Font fontBlob zugeordnet werden kann. |
| fontBlob | byte[] | Byte‑Array mit den Font‑Daten. |
| faceIndex | int | Ein Index des Schriftschnitts in der TrueType‑Schriftartsammlung, oder 0, wenn fontBlob keine TrueType‑Schriftartsammlung ist. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int}
```
public abstract ITextShaper getTextShaper(String fontPath, int faceIndex)
```


Gibt eine neue Instanz eines Text‑Shapers für die Schrift zurück, die durch  fontPath  und  faceIndex  angegeben ist.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontPath | java.lang.String | Ein absoluter Pfad zur Schriftdatei. |
| faceIndex | int | Ein Index des Schriftschnitts in der TrueType‑Schriftartsammlung, oder 0, wenn die angegebene Schriftdatei keine TrueType‑Schriftartsammlung ist. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
