---
title: "FolderFontSource"
linktitle: "FolderFontSource"
second_title: "Aspose.Words لـ Java"
description: "يمثل المجلد الذي يحتوي على ملفات خطوط TrueType في جافا."
type: docs
weight: 318
url: /ar/java/com.aspose.words/folderfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class FolderFontSource extends FontSourceBase
```

يمثل المجلد الذي يحتوي على ملفات خطوط TrueType.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fonts ][Working with Fonts].

 **Examples:** 

يظهر كيفية استخدام مجلد نظام محلي يحتوي على خطوط كمصدر للخطوط.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [FolderFontSource(String folderPath, boolean scanSubfolders)](#FolderFontSource-java.lang.String-boolean) | المُنشئ. |
| [FolderFontSource(String folderPath, boolean scanSubfolders, int priority)](#FolderFontSource-java.lang.String-boolean-int) | المُنشئ. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | يرجع قائمة الخطوط المتاحة عبر هذا المصدر. |
| [getFolderPath()](#getFolderPath) | المسار إلى المجلد. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | يرجع أولوية مصدر الخط. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getScanSubfolders()](#getScanSubfolders) | يحدد ما إذا كان يجب فحص المجلدات الفرعية أم لا. |
| [getType()](#getType) | يرجع نوع مصدر الخط. |
| [getWarningCallback()](#getWarningCallback) | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
### FolderFontSource(String folderPath, boolean scanSubfolders) {#FolderFontSource-java.lang.String-boolean}
```
public FolderFontSource(String folderPath, boolean scanSubfolders)
```


المُنشئ.

 **Examples:** 

يظهر كيفية استخدام مجلد نظام محلي يحتوي على خطوط كمصدر للخطوط.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| folderPath | java.lang.String | المسار إلى المجلد. |
| scanSubfolders | boolean | يحدد ما إذا كان يجب فحص المجلدات الفرعية أم لا. |

### FolderFontSource(String folderPath, boolean scanSubfolders, int priority) {#FolderFontSource-java.lang.String-boolean-int}
```
public FolderFontSource(String folderPath, boolean scanSubfolders, int priority)
```


المُنشئ.

 **Examples:** 

يظهر كيفية استخدام مجلد نظام محلي يحتوي على خطوط كمصدر للخطوط.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| folderPath | java.lang.String | المسار إلى المجلد. |
| scanSubfolders | boolean | يحدد ما إذا كان يجب فحص المجلدات الفرعية أم لا. |
| priority | int | أولوية مصدر الخط. راجع وصف الخاصية [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) لمزيد من المعلومات. |

### getAvailableFonts() {#getAvailableFonts}
```
public ArrayList getAvailableFonts()
```


يرجع قائمة الخطوط المتاحة عبر هذا المصدر.

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
java.util.ArrayList
### getFolderPath() {#getFolderPath}
```
public String getFolderPath()
```


المسار إلى المجلد.

 **Examples:** 

يظهر كيفية استخدام مجلد نظام محلي يحتوي على خطوط كمصدر للخطوط.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getFontDataInternal() {#getFontDataInternal}
```
public Iterable getFontDataInternal()
```




**Returns:**
java.lang.Iterable
### getPriority() {#getPriority}
```
public int getPriority()
```


يرجع أولوية مصدر الخط.

 **Remarks:** 

تُستخدم هذه القيمة عندما تكون هناك خطوط بنفس اسم العائلة والنمط في مصادر خطوط مختلفة. في هذه الحالة يختار Aspose.Words الخط من المصدر الذي لديه قيمة أولوية أعلى.

القيمة الافتراضية هي 0.

 **Examples:** 

يوضح كيفية استخدام ملف خط في نظام الملفات المحلي كمصدر للخط.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```

**Returns:**
int - أولوية مصدر الخط.
### getPriorityInternal() {#getPriorityInternal}
```
public int getPriorityInternal()
```




**Returns:**
int
### getScanSubfolders() {#getScanSubfolders}
```
public boolean getScanSubfolders()
```


يحدد ما إذا كان يجب فحص المجلدات الفرعية أم لا.

 **Examples:** 

يظهر كيفية استخدام مجلد نظام محلي يحتوي على خطوط كمصدر للخطوط.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getType() {#getType}
```
public int getType()
```


يرجع نوع مصدر الخط.

 **Examples:** 

يظهر كيفية استخدام مجلد نظام محلي يحتوي على خطوط كمصدر للخطوط.

```

 // Create a font source from a folder that contains font files.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false, 1);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{folderFontSource});

 Assert.assertEquals(getFontsDir(), folderFontSource.getFolderPath());
 Assert.assertEquals(false, folderFontSource.getScanSubfolders());
 Assert.assertEquals(FontSourceType.FONTS_FOLDER, folderFontSource.getType());
 Assert.assertEquals(1, folderFontSource.getPriority());
 
```

**Returns:**
int - نوع مصدر الخط. القيمة المرجعة هي واحدة من ثوابت [FontSourceType](../../com.aspose.words/fontsourcetype/).
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق.

 **Examples:** 

يوضح كيفية استدعاء رد الاتصال التحذيري عندما تعمل مصادر الخط معًا.

```

 public void fontSourceWarning()
 {
     FontSettings settings = new FontSettings();
     settings.setFontsFolder("bad folder?", false);

     FontSourceBase source = settings.getFontsSources()[0];
     FontSourceWarningCollector callback = new FontSourceWarningCollector();
     source.setWarningCallback(callback);

     // Get the list of fonts to call warning callback.
     ArrayList fontInfos = source.getAvailableFonts();

     Assert.assertEquals("Error loading font from the folder \"bad folder?\": ",
         callback.FontSubstitutionWarnings.get(0).getDescription());
 }

 private static class FontSourceWarningCollector implements IWarningCallback
 {
     /// 
     /// Called every time a warning occurs during processing of font source.
     /// 
     public void warning(WarningInfo info)
     {
         FontSubstitutionWarnings.warning(info);
     }

     public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
 }
 
```

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق.

 **Examples:** 

يوضح كيفية استدعاء رد الاتصال التحذيري عندما تعمل مصادر الخط معًا.

```

 public void fontSourceWarning()
 {
     FontSettings settings = new FontSettings();
     settings.setFontsFolder("bad folder?", false);

     FontSourceBase source = settings.getFontsSources()[0];
     FontSourceWarningCollector callback = new FontSourceWarningCollector();
     source.setWarningCallback(callback);

     // Get the list of fonts to call warning callback.
     ArrayList fontInfos = source.getAvailableFonts();

     Assert.assertEquals("Error loading font from the folder \"bad folder?\": ",
         callback.FontSubstitutionWarnings.get(0).getDescription());
 }

 private static class FontSourceWarningCollector implements IWarningCallback
 {
     /// 
     /// Called every time a warning occurs during processing of font source.
     /// 
     public void warning(WarningInfo info)
     {
         FontSubstitutionWarnings.warning(info);
     }

     public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | القيمة المقابلة لـ [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

