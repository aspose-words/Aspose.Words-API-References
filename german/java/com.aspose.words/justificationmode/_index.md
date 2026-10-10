---
title: "JustificationMode"
linktitle: "JustificationMode"
second_title: "Aspose.Words für Java"
description: "Gibt die Zeichenabstandsanpassung für ein Dokument in Java an."
type: docs
weight: 411
url: /de/java/com.aspose.words/justificationmode/
---

**Inheritance:**
java.lang.Object
```
public class JustificationMode
```

Gibt die Zeichenabstandsanpassung für ein Dokument an. Der Standardwert ist  Expand .

 **Examples:** 

Zeigt, wie man die Zeichenabstandskontrolle verwaltet.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 int justificationMode = doc.getJustificationMode();
 if (justificationMode == JustificationMode.EXPAND)
     doc.setJustificationMode(JustificationMode.COMPRESS);

 doc.save(getArtifactsDir() + "Document.SetJustificationMode.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [COMPRESS](#COMPRESS) | Zeichenabstand komprimieren. |
| [COMPRESS_KANA](#COMPRESS-KANA) | Komprimieren nach den Regeln der Kana‑Silbenschriften, Hiragana und Katakana. |
| [EXPAND](#EXPAND) | Zeichenabstand nicht komprimieren. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String justificationModeName)](#fromName-java.lang.String) |  |
| [getName(int justificationMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int justificationMode)](#toString-int) |  |
### COMPRESS {#COMPRESS}
```
public static int COMPRESS
```


Zeichenabstand komprimieren.

### COMPRESS_KANA {#COMPRESS-KANA}
```
public static int COMPRESS_KANA
```


Komprimieren nach den Regeln der Kana‑Silbenschriften, Hiragana und Katakana.

### EXPAND {#EXPAND}
```
public static int EXPAND
```


Zeichenabstand nicht komprimieren.

### length {#length}
```
public static int length
```


### fromName(String justificationModeName) {#fromName-java.lang.String}
```
public static int fromName(String justificationModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| justificationModeName | java.lang.String |  |

**Returns:**
int
### getName(int justificationMode) {#getName-int}
```
public static String getName(int justificationMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int justificationMode) {#toString-int}
```
public static String toString(int justificationMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
