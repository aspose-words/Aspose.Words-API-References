---
title: TextWrapping
linktitle: TextWrapping
second_title: Aspose.Words for Java
description: Specifies how text is wrapped around the table in Java.
type: docs
weight: 632
url: /java/com.aspose.words/textwrapping/
---

**Inheritance:**
java.lang.Object
```
public class TextWrapping
```

Specifies how text is wrapped around the table.

 **Examples:** 

Shows how to work with table text wrapping.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 builder.getFont().setSize(16.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 // Set the "TextWrapping" property to "TextWrapping.Around" to get the table to wrap text around it,
 // and push it down into the paragraph below by setting the position.
 table.setTextWrapping(TextWrapping.AROUND);
 table.setAbsoluteHorizontalDistance(100.0);
 table.setAbsoluteVerticalDistance(20.0);

 doc.save(getArtifactsDir() + "Table.WrapText.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [AROUND](#AROUND) | Text is wrapped around the table occupying available side space. |
| [DEFAULT](#DEFAULT) | Default value. |
| [NONE](#NONE) | Text and table is displayed in the order of their appearance in the document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String textWrappingName)](#fromName-java.lang.String) |  |
| [getName(int textWrapping)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textWrapping)](#toString-int) |  |
### AROUND {#AROUND}
```
public static int AROUND
```


Text is wrapped around the table occupying available side space.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Default value.

### NONE {#NONE}
```
public static int NONE
```


Text and table is displayed in the order of their appearance in the document.

### length {#length}
```
public static int length
```


### fromName(String textWrappingName) {#fromName-java.lang.String}
```
public static int fromName(String textWrappingName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textWrappingName | java.lang.String |  |

**Returns:**
int
### getName(int textWrapping) {#getName-int}
```
public static String getName(int textWrapping)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textWrapping | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textWrapping) {#toString-int}
```
public static String toString(int textWrapping)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textWrapping | int |  |

**Returns:**
java.lang.String
