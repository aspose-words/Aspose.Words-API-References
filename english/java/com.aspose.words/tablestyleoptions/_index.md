---
title: TableStyleOptions
linktitle: TableStyleOptions
second_title: Aspose.Words for Java
description: Specifies how table style is applied to a table in Java.
type: docs
weight: 657
url: /java/com.aspose.words/tablestyleoptions/
---

**Inheritance:**
java.lang.Object
```
public class TableStyleOptions
```

Specifies how table style is applied to a table.

 **Examples:** 

Shows how to build a new table while applying a style.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // We must insert at least one row before setting any table formatting.
 builder.insertCell();

 // Set the table style used based on the style identifier.
 // Note that not all table styles are available when saving to .doc format.
 table.setStyleIdentifier(StyleIdentifier.MEDIUM_SHADING_1_ACCENT_1);

 // Partially apply the style to features of the table based on predicates, then build the table.
 table.setStyleOptions(TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS | TableStyleOptions.FIRST_ROW);
 table.autoFit(AutoFitBehavior.AUTO_FIT_TO_CONTENTS);

 builder.writeln("Item");
 builder.getCellFormat().setRightPadding(40.0);
 builder.insertCell();
 builder.writeln("Quantity (kg)");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Apples");
 builder.insertCell();
 builder.writeln("20");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Bananas");
 builder.insertCell();
 builder.writeln("40");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Carrots");
 builder.insertCell();
 builder.writeln("50");
 builder.endRow();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithStyle.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [COLUMN_BANDS](#COLUMN-BANDS) | Apply column banding conditional formatting. |
| [DEFAULT](#DEFAULT) | This is Microsoft Word defaults. |
| [DEFAULT_2003](#DEFAULT-2003) | Row and column banding is applied. |
| [FIRST_COLUMN](#FIRST-COLUMN) | Apply 1 first column conditional formatting. |
| [FIRST_ROW](#FIRST-ROW) | Apply first row conditional formatting. |
| [LAST_COLUMN](#LAST-COLUMN) | Apply last column conditional formatting. |
| [LAST_ROW](#LAST-ROW) | Apply last row conditional formatting. |
| [NONE](#NONE) | No table style formatting is applied. |
| [ROW_BANDS](#ROW-BANDS) | Apply row banding conditional formatting. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String tableStyleOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set tableStyleOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int tableStyleOptions)](#getName-int) |  |
| [getNames(int tableStyleOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableStyleOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### COLUMN_BANDS {#COLUMN-BANDS}
```
public static int COLUMN_BANDS
```


Apply column banding conditional formatting.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


This is Microsoft Word defaults.

### DEFAULT_2003 {#DEFAULT-2003}
```
public static int DEFAULT_2003
```


Row and column banding is applied. This is Microsoft Word default for old formats such as DOC, WML and RTF.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


Apply 1 first column conditional formatting.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


Apply first row conditional formatting.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Apply last column conditional formatting.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Apply last row conditional formatting.

### NONE {#NONE}
```
public static int NONE
```


No table style formatting is applied.

### ROW_BANDS {#ROW-BANDS}
```
public static int ROW_BANDS
```


Apply row banding conditional formatting.

### length {#length}
```
public static int length
```


### fromName(String tableStyleOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String tableStyleOptionsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableStyleOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set tableStyleOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set tableStyleOptionsNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableStyleOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int tableStyleOptions) {#getName-int}
```
public static String getName(int tableStyleOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### getNames(int tableStyleOptions) {#getNames-int}
```
public static Set getNames(int tableStyleOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tableStyleOptions) {#toString-int}
```
public static String toString(int tableStyleOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
