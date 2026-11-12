---
title: "TextFormFieldType"
linktitle: "TextFormFieldType"
second_title: "Aspose.Words для Java"
description: "Указывает тип текстового поля формы в Java."
type: docs
weight: 674
url: /ru/java/com.aspose.words/textformfieldtype/
---

**Inheritance:**
java.lang.Object
```
public class TextFormFieldType
```

Указывает тип текстового поля формы.

 **Examples:** 

Показывает, как создавать поля формы.

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
## Поля

| Поле | Описание |
| --- | --- |
| [CALCULATED](#CALCULATED) | Значение текстового поля формы вычисляется из выражения, указанного в свойстве [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String). |
| [CURRENT_DATE](#CURRENT-DATE) | Значение текстового поля формы — текущая дата при обновлении поля. |
| [CURRENT_TIME](#CURRENT-TIME) | Значение текстового поля формы — текущее время при обновлении поля. |
| [DATE](#DATE) | Текстовое поле формы может содержать только корректное значение даты. |
| [NUMBER](#NUMBER) | Текстовое поле формы может содержать только числа. |
| [REGULAR](#REGULAR) | Текстовое поле формы может содержать любой текст. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String textFormFieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int textFormFieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textFormFieldType)](#toString-int) |  |
### CALCULATED {#CALCULATED}
```
public static int CALCULATED
```


Значение текстового поля формы вычисляется из выражения, указанного в свойстве [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String).

### CURRENT_DATE {#CURRENT-DATE}
```
public static int CURRENT_DATE
```


Значение текстового поля формы — текущая дата при обновлении поля.

### CURRENT_TIME {#CURRENT-TIME}
```
public static int CURRENT_TIME
```


Значение текстового поля формы — текущее время при обновлении поля.

### DATE {#DATE}
```
public static int DATE
```


Текстовое поле формы может содержать только корректное значение даты.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


Текстовое поле формы может содержать только числа.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


Текстовое поле формы может содержать любой текст.

### length {#length}
```
public static int length
```


### fromName(String textFormFieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String textFormFieldTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| textFormFieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int textFormFieldType) {#getName-int}
```
public static String getName(int textFormFieldType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| textFormFieldType | int |  |

**Returns:**
java.lang.String
