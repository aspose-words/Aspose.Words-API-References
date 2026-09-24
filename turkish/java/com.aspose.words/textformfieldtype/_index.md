---
title: "TextFormFieldType"
linktitle: "TextFormFieldType"
second_title: "Aspose.Words Java için"
description: "Java'da bir metin form alanının türünü belirtir."
type: docs
weight: 674
url: /tr/java/com.aspose.words/textformfieldtype/
---

**Inheritance:**
java.lang.Object
```
public class TextFormFieldType
```

Bir metin form alanının türünü belirtir.

 **Examples:** 

Form alanları oluşturmanın nasıl yapılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CALCULATED](#CALCULATED) | Metin form alanı değeri, [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String) özelliğinde belirtilen ifadeden hesaplanır. |
| [CURRENT_DATE](#CURRENT-DATE) | Metin form alanı değeri, alan güncellendiğinde geçerli tarih olur. |
| [CURRENT_TIME](#CURRENT-TIME) | Metin form alanı değeri, alan güncellendiğinde geçerli zaman olur. |
| [DATE](#DATE) | Metin form alanı yalnızca geçerli bir tarih değeri içerebilir. |
| [NUMBER](#NUMBER) | Metin form alanı yalnızca sayılar içerebilir. |
| [REGULAR](#REGULAR) | Metin form alanı herhangi bir metin içerebilir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String textFormFieldTypeName)](#fromName-java.lang.String) |  |
| [getName(int textFormFieldType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textFormFieldType)](#toString-int) |  |
### CALCULATED {#CALCULATED}
```
public static int CALCULATED
```


Metin form alanı değeri, [FormField.getTextInputDefault()](../../com.aspose.words/formfield/\#getTextInputDefault) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield/\#setTextInputDefault-java.lang.String) özelliğinde belirtilen ifadeden hesaplanır.

### CURRENT_DATE {#CURRENT-DATE}
```
public static int CURRENT_DATE
```


Metin form alanı değeri, alan güncellendiğinde geçerli tarih olur.

### CURRENT_TIME {#CURRENT-TIME}
```
public static int CURRENT_TIME
```


Metin form alanı değeri, alan güncellendiğinde geçerli zaman olur.

### DATE {#DATE}
```
public static int DATE
```


Metin form alanı yalnızca geçerli bir tarih değeri içerebilir.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


Metin form alanı yalnızca sayılar içerebilir.

### REGULAR {#REGULAR}
```
public static int REGULAR
```


Metin form alanı herhangi bir metin içerebilir.

### length {#length}
```
public static int length
```


### fromName(String textFormFieldTypeName) {#fromName-java.lang.String}
```
public static int fromName(String textFormFieldTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textFormFieldTypeName | java.lang.String |  |

**Returns:**
int
### getName(int textFormFieldType) {#getName-int}
```
public static String getName(int textFormFieldType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textFormFieldType | int |  |

**Returns:**
java.lang.String
