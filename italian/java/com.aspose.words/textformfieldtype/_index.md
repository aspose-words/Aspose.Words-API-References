---
title: "TextFormFieldType"
linktitle: "TextFormFieldType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di campo di modulo di testo in Java."
type: docs
weight: 674
url: /it/java/com.aspose.words/textformfieldtype/
---

**Inheritance:**
java.lang.Object
```
public class TextFormFieldType
```

Specifica il tipo di un campo modulo di testo.

 **Examples:** 

Mostra come creare campi modulo.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CALCULATED](#CALCULATED) | Il valore del campo di modulo di testo è calcolato dall'espressione specificata nella proprietà [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String). |
| [CURRENT_DATE](#CURRENT-DATE) | Il valore del campo di modulo di testo è la data corrente quando il campo viene aggiornato. |
| [CURRENT_TIME](#CURRENT-TIME) | Il valore del campo di modulo di testo è l'ora corrente quando il campo viene aggiornato. |
| [DATE](#DATE) | Il campo di modulo di testo può contenere solo un valore di data valido. |
| [NUMBER](#NUMBER) | Il campo di modulo di testo può contenere solo numeri. |
| [REGULAR](#REGULAR) | Il campo di modulo di testo può contenere qualsiasi testo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String textFormFieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int textFormFieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textFormFieldType)](#toString-int) |  |
### CALCULATED {#CALCULATED}
```
public static int CALCULATED
```


Il valore del campo di modulo di testo è calcolato dall'espressione specificata nella proprietà [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String).

### CURRENT_DATE {#CURRENT-DATE}
```
public static int CURRENT_DATE
```


Il valore del campo di modulo di testo è la data corrente quando il campo viene aggiornato.

### CURRENT_TIME {#CURRENT-TIME}
```
public static int CURRENT_TIME
```


Il valore del campo di modulo di testo è l'ora corrente quando il campo viene aggiornato.

### DATE {#DATE}
```
public static int DATE
```


Il campo di modulo di testo può contenere solo un valore di data valido.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


Il campo di modulo di testo può contenere solo numeri.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


Il campo di modulo di testo può contenere qualsiasi testo.

### length {#length}
```
public static int length
```


### fromName(String textFormFieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String textFormFieldTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textFormFieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int textFormFieldType) {#getName-int}
```
public static String getName(int textFormFieldType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textFormFieldType | int |  |

**Returns:**
java.lang.String
