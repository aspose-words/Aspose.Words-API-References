---
title: AutoFitBehavior
second_title: Aspose.Words for Java API Reference
description: Determines how Aspose.Words resizes the table when you invoke the MAspose.Words.Tables.Table.AutoFitAspose.Words.Tables.AutoFitBehavior method.
type: docs
weight: 15
url: /java/com.aspose.words/autofitbehavior/
---

**Inheritance:**
java.lang.Object
```
public class AutoFitBehavior
```

Determines how Aspose.Words resizes the table when you invoke the **M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)** method.
## Fields

| Field | Description |
| --- | --- |
| [AUTO_FIT_TO_CONTENTS](#AUTO-FIT-TO-CONTENTS) | Aspose.Words enables the AutoFit option, removes the preferred width from the table and all cells and then updates the table layout. |
| [AUTO_FIT_TO_WINDOW](#AUTO-FIT-TO-WINDOW) | When you use this value, Aspose.Words enables the AutoFit option, sets the preferred width for the table to 100%, removes preferred widths from all cells and then updates the table layout. |
| [FIXED_COLUMN_WIDTHS](#FIXED-COLUMN-WIDTHS) | Aspose.Words disables the AutoFit option and removes the preferred with from the table. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int autoFitBehavior)](#getName-int-) |  |
| [toString(int autoFitBehavior)](#toString-int-) |  |
| [fromName(String autoFitBehaviorName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### AUTO_FIT_TO_CONTENTS {#AUTO-FIT-TO-CONTENTS}
```
public static int AUTO_FIT_TO_CONTENTS
```


Aspose.Words enables the AutoFit option, removes the preferred width from the table and all cells and then updates the table layout.

In the resulting table, cell widths are updated to fit the table contents. Most likely, the table will shrink.

### AUTO_FIT_TO_WINDOW {#AUTO-FIT-TO-WINDOW}
```
public static int AUTO_FIT_TO_WINDOW
```


When you use this value, Aspose.Words enables the AutoFit option, sets the preferred width for the table to 100%, removes preferred widths from all cells and then updates the table layout.

As a result, the table occupies all available width and the cell widths are updated to fit table contents.

### FIXED_COLUMN_WIDTHS {#FIXED-COLUMN-WIDTHS}
```
public static int FIXED_COLUMN_WIDTHS
```


Aspose.Words disables the AutoFit option and removes the preferred with from the table.

The widths of the cells remain as they are specified by their [CellFormat.getWidth()](../../com.aspose.words/cellformat\#getWidth--) / [CellFormat.setWidth(double)](../../com.aspose.words/cellformat\#setWidth-double-) properties.

### length {#length}
```
public static int length
```


### getName(int autoFitBehavior) {#getName-int-}
```
public static String getName(int autoFitBehavior)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| autoFitBehavior | int |  |

**Returns:**
java.lang.String
### toString(int autoFitBehavior) {#toString-int-}
```
public static String toString(int autoFitBehavior)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| autoFitBehavior | int |  |

**Returns:**
java.lang.String
### fromName(String autoFitBehaviorName) {#fromName-java.lang.String-}
```
public static int fromName(String autoFitBehaviorName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| autoFitBehaviorName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
