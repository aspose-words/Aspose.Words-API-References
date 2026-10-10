---
title: "PhysicalFontInfo"
linktitle: "PhysicalFontInfo"
second_title: "Aspose.Words لـ Java"
description: "يحدد معلومات حول الخط الفعلي المتاح لمحرك خطوط Aspose.Words في Java."
type: docs
weight: 548
url: /ar/java/com.aspose.words/physicalfontinfo/
---

**Inheritance:**
java.lang.Object
```
public class PhysicalFontInfo
```

يحدد معلومات حول الخط الفيزيائي المتاح لمحرك الخطوط في Aspose.Words.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fonts ][Working with Fonts].

 **Examples:** 

يوضح كيفية سرد الخطوط المتاحة.

```

 // Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
 FontSourceBase[] folderFontSource = {new FolderFontSource(getFontsDir(), true)};

 for (PhysicalFontInfo fontInfo : folderFontSource[0].getAvailableFonts()) {
     System.out.println(MessageFormat.format("FontFamilyName : {0}", fontInfo.getFontFamilyName()));
     System.out.println(MessageFormat.format("FullFontName  : {0}", fontInfo.getFullFontName()));
     System.out.println(MessageFormat.format("Version  : {0}", fontInfo.getVersion()));
     System.out.println(MessageFormat.format("FilePath : {0}\n", fontInfo.getFilePath()));
 }
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getEmbeddingLicensingRights()](#getEmbeddingLicensingRights) | حقوق ترخيص تضمين الخط. |
| [getFilePath()](#getFilePath) | المسار إلى ملف الخط إن وجد. |
| [getFontFamilyName()](#getFontFamilyName) | اسم عائلة الخط. |
| [getFullFontName()](#getFullFontName) | الاسم الكامل للخط. |
| [getVersion()](#getVersion) | سلسلة إصدار الخط. |
### getEmbeddingLicensingRights() {#getEmbeddingLicensingRights}
```
public FontEmbeddingLicensingRights getEmbeddingLicensingRights()
```


حقوق ترخيص تضمين الخط.

 **Examples:** 

يظهر كيفية الحصول على معلومات حقوق الترخيص للخطوط المدمجة (PhysicalFontInfo).

```

 FontSettings settings = FontSettings.getDefaultInstance();
 FontSourceBase source = settings.getFontsSources()[0];

 // Get the list of available fonts.
 ArrayList fontInfos = source.getAvailableFonts();
 for (PhysicalFontInfo fontInfo : fontInfos)
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
[FontEmbeddingLicensingRights](../../com.aspose.words/fontembeddinglicensingrights/) - The corresponding [FontEmbeddingLicensingRights](../../com.aspose.words/fontembeddinglicensingrights/) value.
### getFilePath() {#getFilePath}
```
public String getFilePath()
```


المسار إلى ملف الخط إن وجد.

 **Examples:** 

يوضح كيفية سرد الخطوط المتاحة.

```

 // Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
 FontSourceBase[] folderFontSource = {new FolderFontSource(getFontsDir(), true)};

 for (PhysicalFontInfo fontInfo : folderFontSource[0].getAvailableFonts()) {
     System.out.println(MessageFormat.format("FontFamilyName : {0}", fontInfo.getFontFamilyName()));
     System.out.println(MessageFormat.format("FullFontName  : {0}", fontInfo.getFullFontName()));
     System.out.println(MessageFormat.format("Version  : {0}", fontInfo.getVersion()));
     System.out.println(MessageFormat.format("FilePath : {0}\n", fontInfo.getFilePath()));
 }
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getFontFamilyName() {#getFontFamilyName}
```
public String getFontFamilyName()
```


اسم عائلة الخط.

 **Examples:** 

يوضح كيفية سرد الخطوط المتاحة.

```

 // Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
 FontSourceBase[] folderFontSource = {new FolderFontSource(getFontsDir(), true)};

 for (PhysicalFontInfo fontInfo : folderFontSource[0].getAvailableFonts()) {
     System.out.println(MessageFormat.format("FontFamilyName : {0}", fontInfo.getFontFamilyName()));
     System.out.println(MessageFormat.format("FullFontName  : {0}", fontInfo.getFullFontName()));
     System.out.println(MessageFormat.format("Version  : {0}", fontInfo.getVersion()));
     System.out.println(MessageFormat.format("FilePath : {0}\n", fontInfo.getFilePath()));
 }
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getFullFontName() {#getFullFontName}
```
public String getFullFontName()
```


الاسم الكامل للخط.

 **Examples:** 

يوضح كيفية سرد الخطوط المتاحة.

```

 // Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
 FontSourceBase[] folderFontSource = {new FolderFontSource(getFontsDir(), true)};

 for (PhysicalFontInfo fontInfo : folderFontSource[0].getAvailableFonts()) {
     System.out.println(MessageFormat.format("FontFamilyName : {0}", fontInfo.getFontFamilyName()));
     System.out.println(MessageFormat.format("FullFontName  : {0}", fontInfo.getFullFontName()));
     System.out.println(MessageFormat.format("Version  : {0}", fontInfo.getVersion()));
     System.out.println(MessageFormat.format("FilePath : {0}\n", fontInfo.getFilePath()));
 }
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getVersion() {#getVersion}
```
public String getVersion()
```


سلسلة إصدار الخط.

 **Examples:** 

يوضح كيفية سرد الخطوط المتاحة.

```

 // Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
 FontSourceBase[] folderFontSource = {new FolderFontSource(getFontsDir(), true)};

 for (PhysicalFontInfo fontInfo : folderFontSource[0].getAvailableFonts()) {
     System.out.println(MessageFormat.format("FontFamilyName : {0}", fontInfo.getFontFamilyName()));
     System.out.println(MessageFormat.format("FullFontName  : {0}", fontInfo.getFullFontName()));
     System.out.println(MessageFormat.format("Version  : {0}", fontInfo.getVersion()));
     System.out.println(MessageFormat.format("FilePath : {0}\n", fontInfo.getFilePath()));
 }
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
