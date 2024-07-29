---
title: HeightRule
linktitle: HeightRule
second_title: Aspose.Words for Java
description: Specifies the rule for determining the height of an object in Java.
type: docs
weight: 349
url: /java/com.aspose.words/heightrule/
---

**Inheritance:**
java.lang.Object
```
public class HeightRule
```

Specifies the rule for determining the height of an object.

 **Examples:** 

Shows how to format rows with a document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | The height will be at least the specified height in points. |
| [AUTO](#AUTO) | The height will grow automatically to accommodate all text inside an object. |
| [EXACTLY](#EXACTLY) | The height is specified exactly in points. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String heightRuleName)](#fromName-java.lang.String) |  |
| [getName(int heightRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int heightRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


The height will be at least the specified height in points. It will grow, if needed, to accommodate all text inside an object.

### AUTO {#AUTO}
```
public static int AUTO
```


The height will grow automatically to accommodate all text inside an object.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


The height is specified exactly in points. Please note that if the text cannot fit inside the object of this height, it will appear truncated.

### length {#length}
```
public static int length
```


### fromName(String heightRuleName) {#fromName-java.lang.String}
```
public static int fromName(String heightRuleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**Returns:**
int
### getName(int heightRule) {#getName-int}
```
public static String getName(int heightRule)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int heightRule) {#toString-int}
```
public static String toString(int heightRule)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
