---
title: "FontEmbeddingLicensingRights"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Aspose.Words لـ Java"
description: "يمثل حقوق ترخيص تضمين الخط في جافا."
type: docs
weight: 321
url: /ar/java/com.aspose.words/fontembeddinglicensingrights/
---

**Inheritance:**
java.lang.Object
```
public class FontEmbeddingLicensingRights
```

يمثل حقوق ترخيص تضمين الخط.

 **Remarks:** 

لمزيد من المعلومات، قم بزيارة [ OpenType specification section ][OpenType specification section] على بوابة Microsoft Typography.

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


[OpenType specification section]: https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBitmapEmbeddingOnly()](#getBitmapEmbeddingOnly) | يشير إلى قيود "Bitmap embedding only". |
| [getEmbeddingUsagePermissions()](#getEmbeddingUsagePermissions) | أذونات الاستخدام. |
| [getNoSubsetting()](#getNoSubsetting) | يشير إلى قيود "No subsetting". |
### getBitmapEmbeddingOnly() {#getBitmapEmbeddingOnly}
```
public boolean getBitmapEmbeddingOnly()
```


يشير إلى قيود "Bitmap embedding only".

 **Remarks:** 

عند تعيين هذه البتة، يمكن تضمين البت ماب فقط الموجودة في الخط. لا يمكن تضمين بيانات المخطط. إذا لم تتوفر أي بت ماب في الخط، يُعتبر الخط غير قابل للتضمين وستفشل خدمات التضمين. تنطبق قيود التضمين الأخرى أيضًا.

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
boolean - القيمة المنطقية المقابلة.
### getEmbeddingUsagePermissions() {#getEmbeddingUsagePermissions}
```
public int getEmbeddingUsagePermissions()
```


أذونات الاستخدام.

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
int - القيمة int المقابلة. القيمة المرجعة هي واحدة من ثوابت [FontEmbeddingUsagePermissions](../../com.aspose.words/fontembeddingusagepermissions/).
### getNoSubsetting() {#getNoSubsetting}
```
public boolean getNoSubsetting()
```


يشير إلى قيود "No subsetting".

 **Remarks:** 

عند تعيين هذه العلامة، يجب عدم تقطيع الخط قبل التضمين. تنطبق قيود التضمين الأخرى أيضًا.

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
boolean - القيمة المنطقية المقابلة.
