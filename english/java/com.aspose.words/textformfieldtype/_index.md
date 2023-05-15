---
title: TextFormFieldType
linktitle: TextFormFieldType
second_title: Aspose.Words for Java
description: Specifies the type of a text form field in Java.
type: docs
weight: 585
url: /java/com.aspose.words/textformfieldtype/
---

**Inheritance:**
java.lang.Object
```
public class TextFormFieldType
```

Specifies the type of a text form field.

 **Examples:** 

Shows how to create form fields.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Form fields are objects in the document that the user can interact with by being prompted to enter values.
 // We can create them using a document builder, and below are two ways of doing so.
 // 1 -  Basic text input:
 builder.insertTextInput("My text input", TextFormFieldType.REGULAR,
         "", "Enter your name here", 30);

 // 2 -  Combo box with prompt text, and a range of possible values:
 String[] items =
         {
                 "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
         };

 builder.insertParagraph();
 builder.insertComboBox("My combo box", items, 0);

 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.CreateForm.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [CALCULATED](#CALCULATED) | The text form field value is calculated from the expression specified in the [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String) property. |
| [CURRENT_DATE](#CURRENT-DATE) | The text form field value is the current date when the field is updated. |
| [CURRENT_TIME](#CURRENT-TIME) | The text form field value is the current time when the field is updated. |
| [DATE](#DATE) | The text form field can contain only a valid date value. |
| [NUMBER](#NUMBER) | The text form field can contain only numbers. |
| [REGULAR](#REGULAR) | The text form field can contain any text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String textFormFieldTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int textFormFieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int textFormFieldType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CALCULATED {#CALCULATED}
```
public static int CALCULATED
```


The text form field value is calculated from the expression specified in the [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String) property.

### CURRENT_DATE {#CURRENT-DATE}
```
public static int CURRENT_DATE
```


The text form field value is the current date when the field is updated.

### CURRENT_TIME {#CURRENT-TIME}
```
public static int CURRENT_TIME
```


The text form field value is the current time when the field is updated.

### DATE {#DATE}
```
public static int DATE
```


The text form field can contain only a valid date value.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


The text form field can contain only numbers.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


The text form field can contain any text.

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
### fromName(String textFormFieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String textFormFieldTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textFormFieldTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int textFormFieldType) {#getName-int}
```
public static String getName(int textFormFieldType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textFormFieldType | int |  |

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
### toString(int textFormFieldType) {#toString-int}
```
public static String toString(int textFormFieldType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textFormFieldType | int |  |

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

