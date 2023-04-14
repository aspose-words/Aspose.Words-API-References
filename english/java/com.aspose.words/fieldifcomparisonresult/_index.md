---
title: FieldIfComparisonResult
linktitle: FieldIfComparisonResult
second_title: Aspose.Words for Java API Reference
description: Specifies the result of the IF field condition evaluation in Java.
type: docs
weight: 203
url: /java/com.aspose.words/fieldifcomparisonresult/
---

**Inheritance:**
java.lang.Object
```
public class FieldIfComparisonResult
```

Specifies the result of the IF field condition evaluation.

 **Examples:** 

Shows how to insert an IF field.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Statement 1: ");
 FieldIf field = (FieldIf) builder.insertField(FieldType.FIELD_IF, true);
 field.setLeftExpression("0");
 field.setComparisonOperator("=");
 field.setRightExpression("1");

 // The IF field will display a string from either its "TrueText" property,
 // or its "FalseText" property, depending on the truth of the statement that we have constructed.
 field.setTrueText("True");
 field.setFalseText("False");
 field.update();

 // In this case, "0 = 1" is incorrect, so the displayed result will be "False".
 Assert.assertEquals(" IF  0 = 1 True False", field.getFieldCode());
 Assert.assertEquals(FieldIfComparisonResult.FALSE, field.evaluateCondition());
 Assert.assertEquals("False", field.getResult());

 builder.write("\nStatement 2: ");
 field = (FieldIf) builder.insertField(FieldType.FIELD_IF, true);
 field.setLeftExpression("5");
 field.setComparisonOperator("=");
 field.setRightExpression("2 + 3");
 field.setTrueText("True");
 field.setFalseText("False");
 field.update();

 // This time the statement is correct, so the displayed result will be "True".
 Assert.assertEquals(" IF  5 = \"2 + 3\" True False", field.getFieldCode());
 Assert.assertEquals(FieldIfComparisonResult.TRUE, field.evaluateCondition());
 Assert.assertEquals("True", field.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.IF.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [ERROR](#ERROR) | There is an error in the condition. |
| [FALSE](#FALSE) | The condition is  false . |
| [TRUE](#TRUE) | The condition is  true . |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String fieldIfComparisonResultName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int fieldIfComparisonResult)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int fieldIfComparisonResult)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### ERROR {#ERROR}
```
public static int ERROR
```


There is an error in the condition.

### FALSE {#FALSE}
```
public static int FALSE
```


The condition is  false .

### TRUE {#TRUE}
```
public static int TRUE
```


The condition is  true .

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String fieldIfComparisonResultName) {#fromName-java.lang.String}
```
public static int fromName(String fieldIfComparisonResultName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldIfComparisonResultName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int fieldIfComparisonResult) {#getName-int}
```
public static String getName(int fieldIfComparisonResult)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldIfComparisonResult | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int fieldIfComparisonResult) {#toString-int}
```
public static String toString(int fieldIfComparisonResult)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldIfComparisonResult | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

