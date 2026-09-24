---
title: "FontFamily"
linktitle: "FontFamily"
second_title: "Aspose.Words Java için"
description: "Java'da font ailesini temsil eder."
type: docs
weight: 324
url: /tr/java/com.aspose.words/fontfamily/
---

**Inheritance:**
java.lang.Object
```
public class FontFamily
```

Yazı tipi ailesini temsil eder.

 **Remarks:** 

Font ailesi, ortak çizgi kalınlığı ve serif özelliklerine sahip fontların bir kümesidir.

 **Examples:** 

Bir belgede her yazı tipine nasıl erişileceğini ve ayrıntıların nasıl yazdırılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | Genel bir aile adını belirtir. |
| [DECORATIVE](#DECORATIVE) | Yeni bir yazı tipini belirtir. |
| [MODERN](#MODERN) | Serifli ya da serifsiz bir tek aralıklı yazı tipini belirtir. |
| [ROMAN](#ROMAN) | Serifli bir orantılı (proporsiyonel) yazı tipini belirtir. |
| [SCRIPT](#SCRIPT) | El yazısı gibi görünmesi için tasarlanmış bir yazı tipini belirtir; örnekler arasında Script ve Cursive bulunur. |
| [SWISS](#SWISS) | Serifsiz bir orantılı (proporsiyonel) yazı tipini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String fontFamilyName)](#fromName-java.lang.String) |  |
| [getName(int fontFamily)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFamily)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Genel bir aile adını belirtir. Bu ad, bir yazı tipi hakkında bilgi bulunmadığında ya da önemsiz olduğunda kullanılır. Varsayılan yazı tipi kullanılır.

### DECORATIVE {#DECORATIVE}
```
public static int DECORATIVE
```


Yeni bir yazı tipini belirtir. Bir örnek Old English'tir.

### MODERN {#MODERN}
```
public static int MODERN
```


Serifli ya da serifsiz bir tek aralıklı yazı tipini belirtir. Tek aralıklı yazı tipleri genellikle modern olur; örnekler arasında Pica, Elite ve Courier New bulunur.

### ROMAN {#ROMAN}
```
public static int ROMAN
```


Serifli bir orantılı yazı tipini belirtir. Bir örnek Times New Roman'dır.

### SCRIPT {#SCRIPT}
```
public static int SCRIPT
```


El yazısı gibi görünmesi için tasarlanmış bir yazı tipini belirtir; örnekler arasında Script ve Cursive bulunur.

### SWISS {#SWISS}
```
public static int SWISS
```


Serifsiz bir orantılı yazı tipini belirtir. Bir örnek Arial'dır.

### length {#length}
```
public static int length
```


### fromName(String fontFamilyName) {#fromName-java.lang.String}
```
public static int fromName(String fontFamilyName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontFamilyName | java.lang.String |  |

**Returns:**
int
### getName(int fontFamily) {#getName-int}
```
public static String getName(int fontFamily)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
