---
title: HtmlOfficeMathOutputMode
linktitle: HtmlOfficeMathOutputMode
second_title: Aspose.Words for Java
description: Specifies how Aspose.Words exports OfficeMath to HTML MHTML and EPUB in Java.
type: docs
weight: 360
url: /java/com.aspose.words/htmlofficemathoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlOfficeMathOutputMode
```

Specifies how Aspose.Words exports OfficeMath to HTML, MHTML and EPUB.

 **Examples:** 

Shows how to specify how to export Microsoft OfficeMath objects to HTML.

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
## Fields

| Field | Description |
| --- | --- |
| [IMAGE](#IMAGE) | OfficeMath is converted to HTML as image specified by ![Image 1][] tag.


[Image 1]:  |
| [MATH_ML](#MATH-ML) | OfficeMath is converted to HTML using MathML. |
| [TEXT](#TEXT) | OfficeMath is converted to HTML as sequence of runs specified by  tags. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String htmlOfficeMathOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int htmlOfficeMathOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlOfficeMathOutputMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


OfficeMath is converted to HTML as image specified by ![Image 1][] tag.


[Image 1]: 

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


OfficeMath is converted to HTML using MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


OfficeMath is converted to HTML as sequence of runs specified by  tags.

### length {#length}
```
public static int length
```


### fromName(String htmlOfficeMathOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlOfficeMathOutputModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlOfficeMathOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlOfficeMathOutputMode) {#getName-int}
```
public static String getName(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

**Returns:**
java.lang.String
