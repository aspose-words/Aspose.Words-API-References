---
title: TextFormFieldType
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 565
url: /java/com.aspose.words/textformfieldtype/
---

**Inheritance:**
java.lang.Object
```
public class TextFormFieldType
```

A utility class providing constants. Specifies the type of a text form field.
## Fields

| Field | Description |
| --- | --- |
| [REGULAR](#REGULAR) | The text form field can contain any text. |
| [NUMBER](#NUMBER) | The text form field can contain only numbers. |
| [DATE](#DATE) | The text form field can contain only a valid date value. |
| [CURRENT_DATE](#CURRENT-DATE) | The text form field value is the current date when the field is updated. |
| [CURRENT_TIME](#CURRENT-TIME) | The text form field value is the current time when the field is updated. |
| [CALCULATED](#CALCULATED) | The text form field value is calculated from the expression specified in the [FormField.getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-) property. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int textFormFieldType)](#getName-int-) |  |
| [toString(int textFormFieldType)](#toString-int-) |  |
| [fromName(String textFormFieldTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### REGULAR {#REGULAR}
```
public static int REGULAR
```


The text form field can contain any text.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


The text form field can contain only numbers.

### DATE {#DATE}
```
public static int DATE
```


The text form field can contain only a valid date value.

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

### CALCULATED {#CALCULATED}
```
public static int CALCULATED
```


The text form field value is calculated from the expression specified in the [FormField.getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-) property.

### length {#length}
```
public static int length
```


### getName(int textFormFieldType) {#getName-int-}
```
public static String getName(int textFormFieldType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textFormFieldType | int |  |

**Returns:**
java.lang.String
### toString(int textFormFieldType) {#toString-int-}
```
public static String toString(int textFormFieldType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textFormFieldType | int |  |

**Returns:**
java.lang.String
### fromName(String textFormFieldTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String textFormFieldTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| textFormFieldTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
