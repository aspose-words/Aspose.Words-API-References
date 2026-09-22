---
title: "TextFormFieldType"
linktitle: "TextFormFieldType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع حقل النموذج النصي في Java."
type: docs
weight: 674
url: /ar/java/com.aspose.words/textformfieldtype/
---

**Inheritance:**
java.lang.Object
```
public class TextFormFieldType
```

يحدد نوع حقل النموذج النصي.

 **Examples:** 

يظهر كيفية إنشاء حقول النموذج.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [CALCULATED](#CALCULATED) | قيمة حقل النموذج النصي تُحسب من التعبير المحدد في الخاصية [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String). |
| [CURRENT_DATE](#CURRENT-DATE) | قيمة حقل النموذج النصي هي التاريخ الحالي عند تحديث الحقل. |
| [CURRENT_TIME](#CURRENT-TIME) | قيمة حقل النموذج النصي هي الوقت الحالي عند تحديث الحقل. |
| [DATE](#DATE) | يمكن لحقل النموذج النصي أن يحتوي فقط على قيمة تاريخ صالحة. |
| [NUMBER](#NUMBER) | يمكن لحقل النموذج النصي أن يحتوي فقط على أرقام. |
| [REGULAR](#REGULAR) | يمكن لحقل النموذج النصي أن يحتوي على أي نص. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String textFormFieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int textFormFieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textFormFieldType)](#toString-int) |  |
### CALCULATED {#CALCULATED}
```
public static int CALCULATED
```


قيمة حقل النموذج النصي تُحسب من التعبير المحدد في الخاصية [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String).

### CURRENT_DATE {#CURRENT-DATE}
```
public static int CURRENT_DATE
```


قيمة حقل النموذج النصي هي التاريخ الحالي عند تحديث الحقل.

### CURRENT_TIME {#CURRENT-TIME}
```
public static int CURRENT_TIME
```


قيمة حقل النموذج النصي هي الوقت الحالي عند تحديث الحقل.

### DATE {#DATE}
```
public static int DATE
```


يمكن لحقل النموذج النصي أن يحتوي فقط على قيمة تاريخ صالحة.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


يمكن لحقل النموذج النصي أن يحتوي فقط على أرقام.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


يمكن لحقل النموذج النصي أن يحتوي على أي نص.

### length {#length}
```
public static int length
```


### fromName(String textFormFieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String textFormFieldTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textFormFieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int textFormFieldType) {#getName-int}
```
public static String getName(int textFormFieldType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
### toString(int textFormFieldType) {#toString-int}
```
public static String toString(int textFormFieldType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textFormFieldType | int |  |

**Returns:**
java.lang.String
