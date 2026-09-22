---
title: "FontInfo"
linktitle: "FontInfo"
second_title: "Aspose.Words لـ Java"
description: "يحدد معلومات حول خط مستخدم في المستند بلغة Java."
type: docs
weight: 326
url: /ar/java/com.aspose.words/fontinfo/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class FontInfo implements Cloneable
```

يحدد معلومات حول الخط المستخدم في المستند.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

لا تقوم بإنشاء مثيلات من هذه الفئة مباشرة. استخدم الخاصية [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) للوصول إلى مجموعة الخطوط المعرفة في المستند.

 **Examples:** 

يظهر كيفية طباعة تفاصيل الخطوط الموجودة في المستند.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAltName()](#getAltName) | يحصل على الاسم البديل للخط. |
| [getCharset()](#getCharset) | يحصل على مجموعة الأحرف للخط. |
| [getEmbeddedFont(int format, int style)](#getEmbeddedFont-int-int) |  |
| [getEmbeddedFontAsOpenType(int style)](#getEmbeddedFontAsOpenType-int) |  |
| [getEmbeddingLicensingRights()](#getEmbeddingLicensingRights) | يحصل على حقوق ترخيص الخط المضمّن. |
| [getFamily()](#getFamily) | يحصل على عائلة الخط التي ينتمي إليها هذا الخط. |
| [getName()](#getName) | يحصل على اسم الخط. |
| [getPanose()](#getPanose) | يحصل على رقم تصنيف نوع الخط وفق نظام PANOSE. |
| [getPitch()](#getPitch) | تشير قيمة العرض إلى ما إذا كان الخط ثابت العرض، أو متباعد نسبياً، أو يعتمد على الإعداد الافتراضي. |
| [isTrueType()](#isTrueType) | يشير إلى أن هذا الخط هو خط TrueType أو OpenType وليس خطًا نقطيًا أو متجهيًا. |
| [isTrueType(boolean value)](#isTrueType-boolean) | يشير إلى أن هذا الخط هو خط TrueType أو OpenType وليس خطًا نقطيًا أو متجهيًا. |
| [setAltName(String value)](#setAltName-java.lang.String) | يضبط الاسم البديل للخط. |
| [setCharset(int value)](#setCharset-int) | يضبط مجموعة الأحرف للخط. |
| [setFamily(int value)](#setFamily-int) | يضبط عائلة الخط التي ينتمي إليها هذا الخط. |
| [setPanose(byte[] value)](#setPanose-byte) | يضبط رقم تصنيف الخط PANOSE. |
| [setPitch(int value)](#setPitch-int) | تشير قيمة العرض إلى ما إذا كان الخط ثابت العرض، أو متباعد نسبياً، أو يعتمد على الإعداد الافتراضي. |
### getAltName() {#getAltName}
```
public String getAltName()
```


يحصل على الاسم البديل للخط.

 **Remarks:** 

لا يمكن أن يكون  null . يمكن أن يكون سلسلة فارغة.

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

**Returns:**
java.lang.String - الاسم البديل للخط.
### getCharset() {#getCharset}
```
public int getCharset()
```


يحصل على مجموعة الأحرف للخط.

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

**Returns:**
int - مجموعة الأحرف للخط.
### getEmbeddedFont(int format, int style) {#getEmbeddedFont-int-int}
```
public byte[] getEmbeddedFont(int format, int style)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| التنسيق | int |  |
| النمط | int |  |

**Returns:**
byte[]
### getEmbeddedFontAsOpenType(int style) {#getEmbeddedFontAsOpenType-int}
```
public byte[] getEmbeddedFontAsOpenType(int style)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| النمط | int |  |

**Returns:**
byte[]
### getEmbeddingLicensingRights() {#getEmbeddingLicensingRights}
```
public FontEmbeddingLicensingRights getEmbeddingLicensingRights()
```


يحصل على حقوق ترخيص الخط المضمّن.

 **Remarks:** 

قد تكون القيمة null إذا لم يكن الخط مضمنًا.

 **Examples:** 

يوضح كيفية الحصول على معلومات حقوق الترخيص للخطوط المضمنة (FontInfo).

```

 Document doc = new Document(getMyDir() + "Embedded font rights.docx");

 // Get the list of document fonts.
 FontInfoCollection fontInfos = doc.getFontInfos();
 for (FontInfo fontInfo : fontInfos)
 {
     if (fontInfo.getEmbeddingLicensingRights() != null)
     {
         System.out.println(fontInfo.getEmbeddingLicensingRights().getEmbeddingUsagePermissions());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getBitmapEmbeddingOnly());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getNoSubsetting());
     }
 }
 
```

**Returns:**
[FontEmbeddingLicensingRights](../../com.aspose.words/fontembeddinglicensingrights/) - The embedded font licensing rights.
### getFamily() {#getFamily}
```
public int getFamily()
```


يحصل على عائلة الخط التي ينتمي إليها هذا الخط.

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

**Returns:**
int - عائلة الخط التي ينتمي إليها هذا الخط. القيمة المرجعة هي واحدة من ثوابت [FontFamily](../../com.aspose.words/fontfamily/).
### getName() {#getName}
```
public String getName()
```


يحصل على اسم الخط.

 **Remarks:** 

لا يمكن أن يكون  null . يمكن أن يكون سلسلة فارغة.

 **Examples:** 

يظهر كيفية طباعة تفاصيل الخطوط الموجودة في المستند.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```

**Returns:**
java.lang.String - اسم الخط.
### getPanose() {#getPanose}
```
public byte[] getPanose()
```


يحصل على رقم تصنيف نوع الخط وفق نظام PANOSE.

 **Remarks:** 

PANOSE هو وصف مدمج من 10 بايت للخصائص البصرية الحرجة للخط، مثل التباين والوزن ونمط السيريف. تمثل الأرقام عائلة الخط، نمط السيريف، الوزن، النسبة، التباين، تنوع الخط، نمط الذراع، شكل الحرف، الخط الأوسط، وارتفاع X.

يمكن أن يكون  null .

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

**Returns:**
byte[] - رقم تصنيف الخط PANOSE.
### getPitch() {#getPitch}
```
public int getPitch()
```


تشير قيمة العرض إلى ما إذا كان الخط ثابت العرض، أو متباعد نسبياً، أو يعتمد على الإعداد الافتراضي.

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

**Returns:**
int - القيمة int المقابلة. القيمة المرجعة هي واحدة من ثوابت [FontPitch](../../com.aspose.words/fontpitch/).
### isTrueType() {#isTrueType}
```
public boolean isTrueType()
```


يشير إلى أن هذا الخط هو خط TrueType أو OpenType على عكس الخط النقطي أو المتجه. القيمة الافتراضية هي  true .

 **Examples:** 

يظهر كيفية طباعة تفاصيل الخطوط الموجودة في المستند.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isTrueType(boolean value) {#isTrueType-boolean}
```
public void isTrueType(boolean value)
```


يشير إلى أن هذا الخط هو خط TrueType أو OpenType على عكس الخط النقطي أو المتجه. القيمة الافتراضية هي  true .

 **Examples:** 

يظهر كيفية طباعة تفاصيل الخطوط الموجودة في المستند.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setAltName(String value) {#setAltName-java.lang.String}
```
public void setAltName(String value)
```


يضبط الاسم البديل للخط.

 **Remarks:** 

لا يمكن أن يكون  null . يمكن أن يكون سلسلة فارغة.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | الاسم البديل للخط. |

### setCharset(int value) {#setCharset-int}
```
public void setCharset(int value)
```


يضبط مجموعة الأحرف للخط.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | مجموعة الأحرف للخط. |

### setFamily(int value) {#setFamily-int}
```
public void setFamily(int value)
```


يضبط عائلة الخط التي ينتمي إليها هذا الخط.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | عائلة الخط التي ينتمي إليها هذا الخط. يجب أن تكون القيمة واحدة من ثوابت [FontFamily](../../com.aspose.words/fontfamily/). |

### setPanose(byte[] value) {#setPanose-byte}
```
public void setPanose(byte[] value)
```


يضبط رقم تصنيف الخط PANOSE.

 **Remarks:** 

PANOSE هو وصف مدمج من 10 بايت للخصائص البصرية الحرجة للخط، مثل التباين والوزن ونمط السيريف. تمثل الأرقام عائلة الخط، نمط السيريف، الوزن، النسبة، التباين، تنوع الخط، نمط الذراع، شكل الحرف، الخط الأوسط، وارتفاع X.

يمكن أن يكون  null .

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | byte[] | رقم تصنيف الخط PANOSE. |

### setPitch(int value) {#setPitch-int}
```
public void setPitch(int value)
```


تشير قيمة العرض إلى ما إذا كان الخط ثابت العرض، أو متباعد نسبياً، أو يعتمد على الإعداد الافتراضي.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة int المقابلة. يجب أن تكون القيمة واحدة من ثوابت [FontPitch](../../com.aspose.words/fontpitch/). |

