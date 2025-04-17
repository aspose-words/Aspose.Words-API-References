---
title: HorizontalRuleAlignment
linktitle: HorizontalRuleAlignment
second_title: Aspose.Words for Java
description: Represents the alignment for the specified horizontal rule in Java.
type: docs
weight: 369
url: /java/com.aspose.words/horizontalrulealignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleAlignment
```

Represents the alignment for the specified horizontal rule.

 **Examples:** 

Shows how to insert a horizontal rule shape, and customize its formatting.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```
## Fields

| Field | Description |
| --- | --- |
| [CENTER](#CENTER) | Aligned to the center. |
| [LEFT](#LEFT) | Aligned to the left. |
| [RIGHT](#RIGHT) | Aligned to the right. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String horizontalRuleAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalRuleAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalRuleAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Aligned to the center.

### LEFT {#LEFT}
```
public static int LEFT
```


Aligned to the left.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Aligned to the right.

### length {#length}
```
public static int length
```


### fromName(String horizontalRuleAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalRuleAlignmentName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| horizontalRuleAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalRuleAlignment) {#getName-int}
```
public static String getName(int horizontalRuleAlignment)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| horizontalRuleAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int horizontalRuleAlignment) {#toString-int}
```
public static String toString(int horizontalRuleAlignment)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| horizontalRuleAlignment | int |  |

**Returns:**
java.lang.String
