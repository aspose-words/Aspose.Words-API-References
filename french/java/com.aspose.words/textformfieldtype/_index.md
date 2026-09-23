---
title: "TextFormFieldType"
linktitle: "TextFormFieldType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type d'un champ de formulaire texte en Java."
type: docs
weight: 674
url: /fr/java/com.aspose.words/textformfieldtype/
---

**Inheritance:**
java.lang.Object
```
public class TextFormFieldType
```

Spécifie le type d’un champ de formulaire texte.

 **Examples:** 

Montre comment créer des champs de formulaire.

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
## Champs

| Champ | Description |
| --- | --- |
| [CALCULATED](#CALCULATED) | La valeur du champ de formulaire texte est calculée à partir de l'expression spécifiée dans la propriété [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String). |
| [CURRENT_DATE](#CURRENT-DATE) | La valeur du champ de formulaire texte est la date actuelle lorsque le champ est mis à jour. |
| [CURRENT_TIME](#CURRENT-TIME) | La valeur du champ de formulaire texte est l'heure actuelle lorsque le champ est mis à jour. |
| [DATE](#DATE) | Le champ de formulaire texte ne peut contenir qu'une valeur de date valide. |
| [NUMBER](#NUMBER) | Le champ de formulaire texte ne peut contenir que des nombres. |
| [REGULAR](#REGULAR) | Le champ de formulaire texte peut contenir n'importe quel texte. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String textFormFieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int textFormFieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textFormFieldType)](#toString-int) |  |
### CALCULATED {#CALCULATED}
```
public static int CALCULATED
```


La valeur du champ de formulaire texte est calculée à partir de l'expression spécifiée dans la propriété [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String).

### CURRENT_DATE {#CURRENT-DATE}
```
public static int CURRENT_DATE
```


La valeur du champ de formulaire texte est la date actuelle lorsque le champ est mis à jour.

### CURRENT_TIME {#CURRENT-TIME}
```
public static int CURRENT_TIME
```


La valeur du champ de formulaire texte est l'heure actuelle lorsque le champ est mis à jour.

### DATE {#DATE}
```
public static int DATE
```


Le champ de formulaire texte ne peut contenir qu'une valeur de date valide.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


Le champ de formulaire texte ne peut contenir que des nombres.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


Le champ de formulaire texte peut contenir n'importe quel texte.

### length {#length}
```
public static int length
```


### fromName(String textFormFieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String textFormFieldTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| textFormFieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int textFormFieldType) {#getName-int}
```
public static String getName(int textFormFieldType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| textFormFieldType | int |  |

**Returns:**
java.lang.String
