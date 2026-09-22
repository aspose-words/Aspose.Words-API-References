---
title: "FontInfoCollection"
linktitle: "FontInfoCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من الخطوط المستخدمة في مستند بلغة Java."
type: docs
weight: 327
url: /ar/java/com.aspose.words/fontinfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FontInfoCollection implements Iterable
```

يمثل مجموعة الخطوط المستخدمة في المستند.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

العناصر هي كائنات [FontInfo](../../com.aspose.words/fontinfo/).

لا تقوم بإنشاء مثيلات من هذه الفئة مباشرة. استخدم خاصية [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) للوصول إلى مجموعة الخطوط المعرفة في المستند.

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

يوضح كيفية حفظ مستند مع خطوط TrueType المضمنة.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [contains(String name)](#contains-java.lang.String) | يحدد ما إذا كانت المجموعة تحتوي على خط بالاسم المحدد. |
| [get(int index)](#get-int) | يحصل على خط في الفهرس المحدد. |
| [get(String name)](#get-java.lang.String) | يوفر الوصول إلى عناصر المجموعة. |
| [getCount()](#getCount) | يحصل على عدد العناصر الموجودة في المجموعة. |
| [getEmbedSystemFonts()](#getEmbedSystemFonts) | يحدد ما إذا كان سيتم تضمين خطوط النظام في المستند أم لا. |
| [getEmbedTrueTypeFonts()](#getEmbedTrueTypeFonts) | يحدد ما إذا كان سيتم تضمين خطوط TrueType في المستند عند حفظه أم لا. |
| [getSaveSubsetFonts()](#getSaveSubsetFonts) | يحدد ما إذا كان سيتم حفظ جزء من خطوط TrueType المضمنة مع المستند أم لا. |
| [iterator()](#iterator) | يعيد كائن مكرّر يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [setEmbedSystemFonts(boolean value)](#setEmbedSystemFonts-boolean) | يحدد ما إذا كان سيتم تضمين خطوط النظام في المستند أم لا. |
| [setEmbedTrueTypeFonts(boolean value)](#setEmbedTrueTypeFonts-boolean) | يحدد ما إذا كان سيتم تضمين خطوط TrueType في المستند عند حفظه أم لا. |
| [setSaveSubsetFonts(boolean value)](#setSaveSubsetFonts-boolean) | يحدد ما إذا كان سيتم حفظ جزء من خطوط TrueType المضمنة مع المستند أم لا. |
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


يحدد ما إذا كانت المجموعة تحتوي على خط بالاسم المحدد.

 **Examples:** 

يعرض معلومات حول الخطوط الموجودة في المستند الفارغ.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم الخط غير حساس لحالة الأحرف للبحث عنه. |

**Returns:**
boolean -  true  إذا تم العثور على العنصر في المجموعة؛ وإلا،  false .
### get(int index) {#get-int}
```
public FontInfo get(int index)
```


يحصل على خط في الفهرس المحدد.

 **Examples:** 

يوضح كيفية استخراج خط مضمّن من مستند وحفظه في نظام الملفات المحلي.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | الفهرس الصفري للخط. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - A font at the specified index.
### get(String name) {#get-java.lang.String}
```
public FontInfo get(String name)
```


يوفر الوصول إلى عناصر المجموعة. يحصل على خط بالاسم المحدد.

 **Examples:** 

يوضح كيفية استخراج خط مضمّن من مستند وحفظه في نظام الملفات المحلي.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم الخط غير حساس لحالة الأحرف للبحث عنه. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - The corresponding [FontInfo](../../com.aspose.words/fontinfo/) value.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد العناصر الموجودة في المجموعة.

 **Examples:** 

يعرض معلومات حول الخطوط الموجودة في المستند الفارغ.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Returns:**
int - عدد العناصر الموجودة في المجموعة.
### getEmbedSystemFonts() {#getEmbedSystemFonts}
```
public boolean getEmbedSystemFonts()
```


يحدد ما إذا كان سيتم تضمين خطوط النظام في المستند أم لا. القيمة الافتراضية لهذه الخاصية هي false.

يعمل هذا الخيار فقط عندما يكون خيار [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) مضبوطًا على true.

 **Remarks:** 

تعيين هذه الخاصية إلى true مفيد إذا كان المستخدم يعمل على نظام شرق آسيوي ويرغب في إنشاء مستند يمكن قراءته من قبل الآخرين الذين لا يمتلكون خطوطًا لتلك اللغة على نظامهم. على سبيل المثال، يمكن لمستخدم على نظام ياباني اختيار تضمين الخطوط في المستند بحيث يكون المستند الياباني قابلًا للقراءة على جميع الأنظمة.

يعمل هذا الخيار فقط مع صيغ DOC و DOCX و RTF.

 **Examples:** 

يوضح كيفية حفظ مستند مع خطوط TrueType المضمنة.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getEmbedTrueTypeFonts() {#getEmbedTrueTypeFonts}
```
public boolean getEmbedTrueTypeFonts()
```


يحدد ما إذا كان سيتم تضمين خطوط TrueType في المستند عند حفظه أم لا. القيمة الافتراضية لهذه الخاصية هي false.

 **Remarks:** 

تضمين خطوط TrueType يسمح للآخرين بعرض المستند بنفس الخطوط المستخدمة في إنشائه، لكنه قد يزيد حجم المستند بشكل كبير.

يعمل هذا الخيار فقط مع صيغ DOC و DOCX و RTF.

 **Examples:** 

يوضح كيفية حفظ مستند مع خطوط TrueType المضمنة.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getSaveSubsetFonts() {#getSaveSubsetFonts}
```
public boolean getSaveSubsetFonts()
```


يحدد ما إذا كان سيتم حفظ جزء من خطوط TrueType المضمنة مع المستند أم لا. القيمة الافتراضية لهذه الخاصية هي false.

يعمل هذا الخيار فقط عندما تكون خاصية [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) مضبوطة على true.

 **Remarks:** 

يعمل هذا الخيار فقط مع صيغ DOC و DOCX و RTF.

 **Examples:** 

يوضح كيفية حفظ مستند مع خطوط TrueType المضمنة.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### iterator() {#iterator}
```
public Iterator iterator()
```


يعيد كائن مكرّر يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة.

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
java.util.Iterator
### setEmbedSystemFonts(boolean value) {#setEmbedSystemFonts-boolean}
```
public void setEmbedSystemFonts(boolean value)
```


يحدد ما إذا كان سيتم تضمين خطوط النظام في المستند أم لا. القيمة الافتراضية لهذه الخاصية هي false.

يعمل هذا الخيار فقط عندما يكون خيار [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) مضبوطًا على true.

 **Remarks:** 

تعيين هذه الخاصية إلى true مفيد إذا كان المستخدم يعمل على نظام شرق آسيوي ويرغب في إنشاء مستند يمكن قراءته من قبل الآخرين الذين لا يمتلكون خطوطًا لتلك اللغة على نظامهم. على سبيل المثال، يمكن لمستخدم على نظام ياباني اختيار تضمين الخطوط في المستند بحيث يكون المستند الياباني قابلًا للقراءة على جميع الأنظمة.

يعمل هذا الخيار فقط مع صيغ DOC و DOCX و RTF.

 **Examples:** 

يوضح كيفية حفظ مستند مع خطوط TrueType المضمنة.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setEmbedTrueTypeFonts(boolean value) {#setEmbedTrueTypeFonts-boolean}
```
public void setEmbedTrueTypeFonts(boolean value)
```


يحدد ما إذا كان سيتم تضمين خطوط TrueType في المستند عند حفظه أم لا. القيمة الافتراضية لهذه الخاصية هي false.

 **Remarks:** 

تضمين خطوط TrueType يسمح للآخرين بعرض المستند بنفس الخطوط المستخدمة في إنشائه، لكنه قد يزيد حجم المستند بشكل كبير.

يعمل هذا الخيار فقط مع صيغ DOC و DOCX و RTF.

 **Examples:** 

يوضح كيفية حفظ مستند مع خطوط TrueType المضمنة.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSaveSubsetFonts(boolean value) {#setSaveSubsetFonts-boolean}
```
public void setSaveSubsetFonts(boolean value)
```


يحدد ما إذا كان سيتم حفظ جزء من خطوط TrueType المضمنة مع المستند أم لا. القيمة الافتراضية لهذه الخاصية هي false.

يعمل هذا الخيار فقط عندما تكون خاصية [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) مضبوطة على true.

 **Remarks:** 

يعمل هذا الخيار فقط مع صيغ DOC و DOCX و RTF.

 **Examples:** 

يوضح كيفية حفظ مستند مع خطوط TrueType المضمنة.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

