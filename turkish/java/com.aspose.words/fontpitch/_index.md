---
title: "FontPitch"
linktitle: "FontPitch"
second_title: "Aspose.Words Java için"
description: "Java'da font pitch'i temsil eder."
type: docs
weight: 330
url: /tr/java/com.aspose.words/fontpitch/
---

**Inheritance:**
java.lang.Object
```
public class FontPitch
```

Yazı tipi aralığını temsil eder.

 **Remarks:** 

Aralık, yazı tipinin sabit aralıklı, orantılı aralıklı olup olmadığını veya varsayılan ayara dayanıp dayanmadığını gösterir.

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
| [DEFAULT](#DEFAULT) | Bir yazı tipinin perdesi (pitch) hakkında bilgi bulunmadığını belirtir. |
| [FIXED](#FIXED) | Bu karakterin sabit genişlikli bir yazı tipi olduğunu belirtir. |
| [VARIABLE](#VARIABLE) | Bu karakterin orantılı genişlikli bir yazı tipi olduğunu belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String fontPitchName)](#fromName-java.lang.String) |  |
| [getName(int fontPitch)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontPitch)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Bir yazı tipinin perdesi (pitch) hakkında bilgi bulunmadığını belirtir.

### FIXED {#FIXED}
```
public static int FIXED
```


Bu karakterin sabit genişlikli bir yazı tipi olduğunu belirtir.

### VARIABLE {#VARIABLE}
```
public static int VARIABLE
```


Bu karakterin orantılı genişlikli bir yazı tipi olduğunu belirtir.

### length {#length}
```
public static int length
```


### fromName(String fontPitchName) {#fromName-java.lang.String}
```
public static int fromName(String fontPitchName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontPitchName | java.lang.String |  |

**Returns:**
int
### getName(int fontPitch) {#getName-int}
```
public static String getName(int fontPitch)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontPitch | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontPitch) {#toString-int}
```
public static String toString(int fontPitch)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontPitch | int |  |

**Returns:**
java.lang.String
