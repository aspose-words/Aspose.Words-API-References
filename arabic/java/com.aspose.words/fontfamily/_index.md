---
title: "FontFamily"
linktitle: "FontFamily"
second_title: "Aspose.Words لـ Java"
description: "يمثل عائلة الخطوط في Java."
type: docs
weight: 324
url: /ar/java/com.aspose.words/fontfamily/
---

**Inheritance:**
java.lang.Object
```
public class FontFamily
```

يمثل عائلة الخط.

 **Remarks:** 

عائلة الخطوط هي مجموعة من الخطوط ذات عرض الخط المشترك وخصائص السيريـف.

 **Examples:** 

يوضح كيفية الوصول إلى وطباعة تفاصيل كل خط في مستند.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Iterator fontCollectionEnumerator = doc.getFontInfos().iterator();
 while (fontCollectionEnumerator.hasNext()) {
     FontInfo fontInfo = fontCollectionEnumerator.next();
     if (fontInfo != null) {
         System.out.println("Font name: " + fontInfo.getName());

         // Alt names are usually blank.
         System.out.println("Alt name: " + fontInfo.getAltName());
         System.out.println("\t- Family: " + fontInfo.getFamily());
         System.out.println("\t- " + (fontInfo.isTrueType() ? "Is TrueType" : "Is not TrueType"));
         System.out.println("\t- Pitch: " + fontInfo.getPitch());
         System.out.println("\t- Charset: " + fontInfo.getCharset());
         System.out.println("\t- Panose:");
         System.out.println("\t\tFamily Kind: " + (fontInfo.getPanose()[0] & 0xFF));
         System.out.println("\t\tSerif Style: " + (fontInfo.getPanose()[1] & 0xFF));
         System.out.println("\t\tWeight: " + (fontInfo.getPanose()[2] & 0xFF));
         System.out.println("\t\tProportion: " + (fontInfo.getPanose()[3] & 0xFF));
         System.out.println("\t\tContrast: " + (fontInfo.getPanose()[4] & 0xFF));
         System.out.println("\t\tStroke Variation: " + (fontInfo.getPanose()[5] & 0xFF));
         System.out.println("\t\tArm Style: " + (fontInfo.getPanose()[6] & 0xFF));
         System.out.println("\t\tLetterform: " + (fontInfo.getPanose()[7] & 0xFF));
         System.out.println("\t\tMidline: " + (fontInfo.getPanose()[8] & 0xFF));
         System.out.println("\t\tX-Height: " + (fontInfo.getPanose()[9] & 0xFF));
     }
 }
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | يحدد اسم عائلة عام. |
| [DECORATIVE](#DECORATIVE) | يحدد خطًا فريدًا. |
| [MODERN](#MODERN) | يحدد خطًا ثابت العرض مع أو بدون حواف. |
| [ROMAN](#ROMAN) | يحدد خطًا متناسبًا مع حواف. |
| [SCRIPT](#SCRIPT) | يحدد خطًا صُمم ليشبه الكتابة اليدوية؛ تشمل الأمثلة Script و Cursive. |
| [SWISS](#SWISS) | يحدد خطًا متناسبًا بدون حواف. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String fontFamilyName)](#fromName-java.lang.String) |  |
| [getName(int fontFamily)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFamily)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


يحدد اسم عائلة عام. يُستخدم هذا الاسم عندما لا تتوفر معلومات عن الخط أو لا تهم. يتم استخدام الخط الافتراضي.

### DECORATIVE {#DECORATIVE}
```
public static int DECORATIVE
```


يحدد خطًا فريدًا. مثال على ذلك هو Old English.

### MODERN {#MODERN}
```
public static int MODERN
```


يحدد خطًا ثابت العرض مع أو بدون حواف. عادةً ما تكون الخطوط ثابتة العرض حديثة؛ تشمل الأمثلة Pica و Elite و Courier New.

### ROMAN {#ROMAN}
```
public static int ROMAN
```


يحدد خطًا متناسبًا مع حواف. مثال على ذلك هو Times New Roman.

### SCRIPT {#SCRIPT}
```
public static int SCRIPT
```


يحدد خطًا صُمم ليشبه الكتابة اليدوية؛ تشمل الأمثلة Script و Cursive.

### SWISS {#SWISS}
```
public static int SWISS
```


يحدد خطًا متناسبًا بدون حواف. مثال على ذلك هو Arial.

### length {#length}
```
public static int length
```


### fromName(String fontFamilyName) {#fromName-java.lang.String}
```
public static int fromName(String fontFamilyName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontFamilyName | java.lang.String |  |

**Returns:**
int
### getName(int fontFamily) {#getName-int}
```
public static String getName(int fontFamily)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontFamily) {#toString-int}
```
public static String toString(int fontFamily)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
