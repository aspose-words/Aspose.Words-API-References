---
title: "TextFormFieldType"
linktitle: "TextFormFieldType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ eines Textformularfelds in Java an."
type: docs
weight: 674
url: /de/java/com.aspose.words/textformfieldtype/
---

**Inheritance:**
java.lang.Object
```
public class TextFormFieldType
```

Gibt den Typ eines Textformularfelds an.

 **Examples:** 

Zeigt, wie Formularfelder erstellt werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CALCULATED](#CALCULATED) | Der Wert des Textformularfelds wird aus dem Ausdruck berechnet, der in der Eigenschaft [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String) angegeben ist. |
| [CURRENT_DATE](#CURRENT-DATE) | Der Wert des Textformularfelds ist das aktuelle Datum, wenn das Feld aktualisiert wird. |
| [CURRENT_TIME](#CURRENT-TIME) | Der Wert des Textformularfelds ist die aktuelle Uhrzeit, wenn das Feld aktualisiert wird. |
| [DATE](#DATE) | Das Textformularfeld kann nur einen gültigen Datumswert enthalten. |
| [NUMBER](#NUMBER) | Das Textformularfeld kann nur Zahlen enthalten. |
| [REGULAR](#REGULAR) | Das Textformularfeld kann beliebigen Text enthalten. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String textFormFieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int textFormFieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textFormFieldType)](#toString-int) |  |
### CALCULATED {#CALCULATED}
```
public static int CALCULATED
```


Der Wert des Textformularfelds wird aus dem Ausdruck berechnet, der in der Eigenschaft [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String) angegeben ist.

### CURRENT_DATE {#CURRENT-DATE}
```
public static int CURRENT_DATE
```


Der Wert des Textformularfelds ist das aktuelle Datum, wenn das Feld aktualisiert wird.

### CURRENT_TIME {#CURRENT-TIME}
```
public static int CURRENT_TIME
```


Der Wert des Textformularfelds ist die aktuelle Uhrzeit, wenn das Feld aktualisiert wird.

### DATE {#DATE}
```
public static int DATE
```


Das Textformularfeld kann nur einen gültigen Datumswert enthalten.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


Das Textformularfeld kann nur Zahlen enthalten.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


Das Textformularfeld kann beliebigen Text enthalten.

### length {#length}
```
public static int length
```


### fromName(String textFormFieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String textFormFieldTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textFormFieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int textFormFieldType) {#getName-int}
```
public static String getName(int textFormFieldType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textFormFieldType | int |  |

**Returns:**
java.lang.String
