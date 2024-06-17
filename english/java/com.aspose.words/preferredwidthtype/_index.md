---
title: PreferredWidthType
linktitle: PreferredWidthType
second_title: Aspose.Words for Java
description: Specifies the unit of measurement for the preferred width of a table or cell in Java.
type: docs
weight: 510
url: /java/com.aspose.words/preferredwidthtype/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidthType
```

Specifies the unit of measurement for the preferred width of a table or cell.

 **Examples:** 

Shows how to verify the preferred width type and value of a table cell.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | The preferred width is not specified. |
| [PERCENT](#PERCENT) | Measure the current item width using a specified percentage. |
| [POINTS](#POINTS) | Measure the current item width using a specified number of points (1/72 inch). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String) |  |
| [getName(int preferredWidthType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int preferredWidthType)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


The preferred width is not specified. The actual width of the table or cell is either specified using the explicit width or will be determined automatically by the table layout algorithm when the table is displayed, depending on the table auto fit setting.

### PERCENT {#PERCENT}
```
public static int PERCENT
```


Measure the current item width using a specified percentage.

### POINTS {#POINTS}
```
public static int POINTS
```


Measure the current item width using a specified number of points (1/72 inch).

### length {#length}
```
public static int length
```


### fromName(String preferredWidthTypeName) {#fromName-java.lang.String}
```
public static int fromName(String preferredWidthTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**Returns:**
int
### getName(int preferredWidthType) {#getName-int}
```
public static String getName(int preferredWidthType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int preferredWidthType) {#toString-int}
```
public static String toString(int preferredWidthType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
