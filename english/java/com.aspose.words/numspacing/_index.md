---
title: NumSpacing
linktitle: NumSpacing
second_title: Aspose.Words for Java
description: Specifies possible values in which numeral spacing can be displayed in Java.
type: docs
weight: 482
url: /java/com.aspose.words/numspacing/
---

**Inheritance:**
java.lang.Object
```
public class NumSpacing
```

Specifies possible values in which numeral spacing can be displayed.

 **Examples:** 

Shows how to set the spacing type of the numeral.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Specifies that numerals are displayed in the font\\u2019s default form. |
| [PROPORTIONAL](#PROPORTIONAL) | Specifies that the forms of the numerals designed as proportionally spaced are displayed if supported by the font. |
| [TABULAR](#TABULAR) | Specifies that the forms of the numerals designed as tabular are displayed if supported by the font. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String numSpacingName)](#fromName-java.lang.String) |  |
| [getName(int numSpacing)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numSpacing)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Specifies that numerals are displayed in the font\\u2019s default form.

### PROPORTIONAL {#PROPORTIONAL}
```
public static int PROPORTIONAL
```


Specifies that the forms of the numerals designed as proportionally spaced are displayed if supported by the font.

### TABULAR {#TABULAR}
```
public static int TABULAR
```


Specifies that the forms of the numerals designed as tabular are displayed if supported by the font.

### length {#length}
```
public static int length
```


### fromName(String numSpacingName) {#fromName-java.lang.String}
```
public static int fromName(String numSpacingName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| numSpacingName | java.lang.String |  |

**Returns:**
int
### getName(int numSpacing) {#getName-int}
```
public static String getName(int numSpacing)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int numSpacing) {#toString-int}
```
public static String toString(int numSpacing)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
