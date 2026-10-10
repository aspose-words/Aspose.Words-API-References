---
title: "HtmlOfficeMathOutputMode"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Aspose.Words OfficeMath in Java nach HTML, MHTML und EPUB exportiert."
type: docs
weight: 384
url: /de/java/com.aspose.words/htmlofficemathoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlOfficeMathOutputMode
```

Gibt an, wie Aspose.Words OfficeMath nach HTML, MHTML und EPUB exportiert.

 **Examples:** 

Zeigt, wie man angibt, wie Microsoft OfficeMath‑Objekte nach HTML exportiert werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles OfficeMath objects.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Image"
 // will render each OfficeMath object into an image.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.MathML"
 // will convert each OfficeMath object into MathML.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Text"
 // will represent each OfficeMath formula using plain HTML text.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setOfficeMathOutputMode(htmlOfficeMathOutputMode);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
|  | [IMAGE](#IMAGE) | OfficeMath wird in HTML als Bild konvertiert, das durch das ![Image 1][]‑Tag angegeben ist. |


[Image 1]:  |
| [MATH_ML](#MATH-ML) | OfficeMath wird in HTML mittels MathML konvertiert. |
| [TEXT](#TEXT) | OfficeMath wird in HTML als Sequenz von Runs konvertiert, die durch  Tags angegeben sind. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String htmlOfficeMathOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int htmlOfficeMathOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlOfficeMathOutputMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


OfficeMath wird in HTML als Bild konvertiert, das durch das ![Image 1][]‑Tag angegeben ist.


[Image 1]: 

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


OfficeMath wird in HTML mittels MathML konvertiert.

### TEXT {#TEXT}
```
public static int TEXT
```


OfficeMath wird in HTML als Sequenz von Runs konvertiert, die durch  Tags angegeben sind.

### length {#length}
```
public static int length
```


### fromName(String htmlOfficeMathOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlOfficeMathOutputModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| htmlOfficeMathOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlOfficeMathOutputMode) {#getName-int}
```
public static String getName(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlOfficeMathOutputMode) {#toString-int}
```
public static String toString(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

**Returns:**
java.lang.String
