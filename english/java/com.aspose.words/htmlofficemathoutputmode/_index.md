---
title: HtmlOfficeMathOutputMode
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 330
url: /java/com.aspose.words/htmlofficemathoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlOfficeMathOutputMode
```

A utility class providing constants. Specifies how Aspose.Words exports OfficeMath to HTML, MHTML and EPUB.
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
| [getName(int htmlOfficeMathOutputMode)](#getName-int-) |  |
| [toString(int htmlOfficeMathOutputMode)](#toString-int-) |  |
| [fromName(String htmlOfficeMathOutputModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
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


### getName(int htmlOfficeMathOutputMode) {#getName-int-}
```
public static String getName(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

**Returns:**
java.lang.String
### toString(int htmlOfficeMathOutputMode) {#toString-int-}
```
public static String toString(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

**Returns:**
java.lang.String
### fromName(String htmlOfficeMathOutputModeName) {#fromName-java.lang.String-}
```
public static int fromName(String htmlOfficeMathOutputModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlOfficeMathOutputModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
