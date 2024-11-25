---
title: EmphasisMark
linktitle: EmphasisMark
second_title: Aspose.Words for Java
description: Specifies possible types of emphasis mark in Java.
type: docs
weight: 177
url: /java/com.aspose.words/emphasismark/
---

**Inheritance:**
java.lang.Object
```
public class EmphasisMark
```

Specifies possible types of emphasis mark.

 **Examples:** 

Shows how to add additional character rendered above/below the glyph-character.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Possible types of emphasis mark:
 // https://apireference.aspose.com/words/net/aspose.words/emphasismark
 builder.getFont().setEmphasisMark(emphasisMark);

 builder.write("Emphasis text");
 builder.writeln();
 builder.getFont().clearFormatting();
 builder.write("Simple text");

 builder.getDocument().save(getArtifactsDir() + "Fonts.SetEmphasisMark.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | No emphasis mark. |
| [OVER_COMMA](#OVER-COMMA) | Emphasis mark is a comma character displayed above text. |
| [OVER_SOLID_CIRCLE](#OVER-SOLID-CIRCLE) | Emphasis mark is a solid black circle displayed above text. |
| [OVER_WHITE_CIRCLE](#OVER-WHITE-CIRCLE) | Emphasis mark is an empty white circle displayed above text. |
| [UNDER_SOLID_CIRCLE](#UNDER-SOLID-CIRCLE) | Emphasis mark is a solid black circle displayed below text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String emphasisMarkName)](#fromName-java.lang.String) |  |
| [getName(int emphasisMark)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int emphasisMark)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


No emphasis mark.

### OVER_COMMA {#OVER-COMMA}
```
public static int OVER_COMMA
```


Emphasis mark is a comma character displayed above text.

### OVER_SOLID_CIRCLE {#OVER-SOLID-CIRCLE}
```
public static int OVER_SOLID_CIRCLE
```


Emphasis mark is a solid black circle displayed above text.

### OVER_WHITE_CIRCLE {#OVER-WHITE-CIRCLE}
```
public static int OVER_WHITE_CIRCLE
```


Emphasis mark is an empty white circle displayed above text.

### UNDER_SOLID_CIRCLE {#UNDER-SOLID-CIRCLE}
```
public static int UNDER_SOLID_CIRCLE
```


Emphasis mark is a solid black circle displayed below text.

### length {#length}
```
public static int length
```


### fromName(String emphasisMarkName) {#fromName-java.lang.String}
```
public static int fromName(String emphasisMarkName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| emphasisMarkName | java.lang.String |  |

**Returns:**
int
### getName(int emphasisMark) {#getName-int}
```
public static String getName(int emphasisMark)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int emphasisMark) {#toString-int}
```
public static String toString(int emphasisMark)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| emphasisMark | int |  |

**Returns:**
java.lang.String
