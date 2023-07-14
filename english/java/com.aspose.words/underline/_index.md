---
title: Underline
linktitle: Underline
second_title: Aspose.Words for Java
description: Indicates type of the underline applied to a font in Java.
type: docs
weight: 612
url: /java/com.aspose.words/underline/
---

**Inheritance:**
java.lang.Object
```
public class Underline
```

Indicates type of the underline applied to a font.

 **Examples:** 

Shows how to insert a hyperlink field.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [DASH](#DASH) |  |
| [DASH_HEAVY](#DASH-HEAVY) |  |
| [DASH_LONG](#DASH-LONG) |  |
| [DASH_LONG_HEAVY](#DASH-LONG-HEAVY) |  |
| [DOTTED](#DOTTED) |  |
| [DOTTED_HEAVY](#DOTTED-HEAVY) |  |
| [DOT_DASH](#DOT-DASH) |  |
| [DOT_DASH_HEAVY](#DOT-DASH-HEAVY) |  |
| [DOT_DOT_DASH](#DOT-DOT-DASH) |  |
| [DOT_DOT_DASH_HEAVY](#DOT-DOT-DASH-HEAVY) |  |
| [DOUBLE](#DOUBLE) |  |
| [NONE](#NONE) |  |
| [SINGLE](#SINGLE) |  |
| [THICK](#THICK) |  |
| [WAVY](#WAVY) |  |
| [WAVY_DOUBLE](#WAVY-DOUBLE) |  |
| [WAVY_HEAVY](#WAVY-HEAVY) |  |
| [WORDS](#WORDS) |  |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String underlineName)](#fromName-java.lang.String) |  |
| [getName(int underline)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int underline)](#toString-int) |  |
### DASH {#DASH}
```
public static int DASH
```




### DASH_HEAVY {#DASH-HEAVY}
```
public static int DASH_HEAVY
```




### DASH_LONG {#DASH-LONG}
```
public static int DASH_LONG
```




### DASH_LONG_HEAVY {#DASH-LONG-HEAVY}
```
public static int DASH_LONG_HEAVY
```




### DOTTED {#DOTTED}
```
public static int DOTTED
```




### DOTTED_HEAVY {#DOTTED-HEAVY}
```
public static int DOTTED_HEAVY
```




### DOT_DASH {#DOT-DASH}
```
public static int DOT_DASH
```




### DOT_DASH_HEAVY {#DOT-DASH-HEAVY}
```
public static int DOT_DASH_HEAVY
```




### DOT_DOT_DASH {#DOT-DOT-DASH}
```
public static int DOT_DOT_DASH
```




### DOT_DOT_DASH_HEAVY {#DOT-DOT-DASH-HEAVY}
```
public static int DOT_DOT_DASH_HEAVY
```




### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```




### NONE {#NONE}
```
public static int NONE
```




### SINGLE {#SINGLE}
```
public static int SINGLE
```




### THICK {#THICK}
```
public static int THICK
```




### WAVY {#WAVY}
```
public static int WAVY
```




### WAVY_DOUBLE {#WAVY-DOUBLE}
```
public static int WAVY_DOUBLE
```




### WAVY_HEAVY {#WAVY-HEAVY}
```
public static int WAVY_HEAVY
```




### WORDS {#WORDS}
```
public static int WORDS
```




### length {#length}
```
public static int length
```


### fromName(String underlineName) {#fromName-java.lang.String}
```
public static int fromName(String underlineName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| underlineName | java.lang.String |  |

**Returns:**
int
### getName(int underline) {#getName-int}
```
public static String getName(int underline)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| underline | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int underline) {#toString-int}
```
public static String toString(int underline)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| underline | int |  |

**Returns:**
java.lang.String
