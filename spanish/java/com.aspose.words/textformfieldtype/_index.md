---
title: "TextFormFieldType"
linktitle: "TextFormFieldType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de un campo de formulario de texto en Java."
type: docs
weight: 674
url: /es/java/com.aspose.words/textformfieldtype/
---

**Inheritance:**
java.lang.Object
```
public class TextFormFieldType
```

Especifica el tipo de un campo de formulario de texto.

 **Examples:** 

Muestra cómo crear campos de formulario.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [CALCULATED](#CALCULATED) | El valor del campo de formulario de texto se calcula a partir de la expresión especificada en la propiedad [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String). |
| [CURRENT_DATE](#CURRENT-DATE) | El valor del campo de formulario de texto es la fecha actual cuando se actualiza el campo. |
| [CURRENT_TIME](#CURRENT-TIME) | El valor del campo de formulario de texto es la hora actual cuando se actualiza el campo. |
| [DATE](#DATE) | El campo de formulario de texto solo puede contener un valor de fecha válido. |
| [NUMBER](#NUMBER) | El campo de formulario de texto solo puede contener números. |
| [REGULAR](#REGULAR) | El campo de formulario de texto puede contener cualquier texto. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String textFormFieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int textFormFieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textFormFieldType)](#toString-int) |  |
### CALCULATED {#CALCULATED}
```
public static int CALCULATED
```


El valor del campo de formulario de texto se calcula a partir de la expresión especificada en la propiedad [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String).

### CURRENT_DATE {#CURRENT-DATE}
```
public static int CURRENT_DATE
```


El valor del campo de formulario de texto es la fecha actual cuando se actualiza el campo.

### CURRENT_TIME {#CURRENT-TIME}
```
public static int CURRENT_TIME
```


El valor del campo de formulario de texto es la hora actual cuando se actualiza el campo.

### DATE {#DATE}
```
public static int DATE
```


El campo de formulario de texto solo puede contener un valor de fecha válido.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


El campo de formulario de texto solo puede contener números.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


El campo de formulario de texto puede contener cualquier texto.

### length {#length}
```
public static int length
```


### fromName(String textFormFieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String textFormFieldTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textFormFieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int textFormFieldType) {#getName-int}
```
public static String getName(int textFormFieldType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textFormFieldType | int |  |

**Returns:**
java.lang.String
