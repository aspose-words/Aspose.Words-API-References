---
title: "StreamFontSource"
linktitle: "StreamFontSource"
second_title: "Aspose.Words لـ Java"
description: "الفئة الأساسية لمصدر خط التدفق المعرّف من قبل المستخدم في Java."
type: docs
weight: 635
url: /ar/java/com.aspose.words/streamfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public abstract class StreamFontSource extends FontSourceBase
```

الفئة الأساسية لمصدر خط تدفق معرف من قبل المستخدم.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

لكي تستخدم مصدر خط التدفق، يجب عليك إنشاء فئة مشتقة من [StreamFontSource](../../com.aspose.words/streamfontsource/) وتوفير تنفيذ للطريقة [openFontDataStream()](../../com.aspose.words/streamfontsource/\#openFontDataStream).

[openFontDataStream()](../../com.aspose.words/streamfontsource/\#openFontDataStream) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](../../com.aspose.words/streamfontsource/) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../../com.aspose.words/fontsettings/) lifetime.

 **Examples:** 

يوضح كيفية تحميل الخطوط من التدفق.

```

 public void streamFontSourceFileRendering() throws Exception {
     FontSettings fontSettings = new FontSettings();
     fontSettings.setFontsSources(new FontSourceBase[]{new StreamFontSourceFile()});

     DocumentBuilder builder = new DocumentBuilder();
     builder.getDocument().setFontSettings(fontSettings);
     builder.getFont().setName("Kreon-Regular");
     builder.writeln("Test aspose text when saving to PDF.");

     builder.getDocument().save(getArtifactsDir() + "FontSettings.StreamFontSourceFileRendering.pdf");
 }

 /// 
 /// Load the font data only when required instead of storing it in the memory for the entire lifetime of the "FontSettings" object.
 /// 
 private static class StreamFontSourceFile extends StreamFontSource  {
     public FileInputStream openFontDataStream() throws Exception {
         return new FileInputStream(getFontsDir() + "Kreon-Regular.ttf");
     }
 }
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | يرجع قائمة الخطوط المتاحة عبر هذا المصدر. |
| [getCacheKey()](#getCacheKey) | المفتاح لهذا المصدر في الذاكرة المؤقتة. |
| [getCacheKeyInternal()](#getCacheKeyInternal) |  |
| [getFilePath()](#getFilePath) |  |
| [getFontBytes()](#getFontBytes) |  |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | يرجع أولوية مصدر الخط. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getSize()](#getSize) |  |
| [getType()](#getType) | يرجع نوع مصدر الخط. |
| [getWarningCallback()](#getWarningCallback) | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| [isEmbedded()](#isEmbedded) |  |
| [openFontDataStream()](#openFontDataStream) | يجب أن تفتح هذه الطريقة التدفق ببيانات الخط عند الطلب. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
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
### getCacheKey() {#getCacheKey}
```
public String getCacheKey()
```


المفتاح لهذا المصدر في الذاكرة المؤقتة.

 **Remarks:** 

يُستخدم هذا المفتاح لتحديد عنصر الذاكرة المؤقتة عند حفظ/تحميل ذاكرة البحث عن الخطوط باستخدام طريقتي  و .

 **Examples:** 

يوضح كيفية تسريع عملية تهيئة ذاكرة الخط المؤقتة.

```

 public void loadFontSearchCache() throws Exception
 {
     final String CACHE_KEY_1 = "Arvo";
     final String CACHE_KEY_2 = "Arvo-Bold";
     FontSettings parsedFonts = new FontSettings();
     FontSettings loadedCache = new FontSettings();

     parsedFonts.setFontsSources(new FontSourceBase[]
             {
                     new FileFontSource(getFontsDir() + "Arvo-Regular.ttf", 0, CACHE_KEY_1),
                     new FileFontSource(getFontsDir() + "Arvo-Bold.ttf", 0, CACHE_KEY_2)
             });

     try (ByteArrayOutputStream cacheStream = new ByteArrayOutputStream())
     {
         parsedFonts.saveSearchCache(cacheStream);
         ByteArrayInputStream inputStream = new ByteArrayInputStream(cacheStream.toByteArray());
         loadedCache.setFontsSources(new FontSourceBase[]
                 {
                         new SearchCacheStream(CACHE_KEY_1),
                         new MemoryFontSource(Files.readAllBytes(Paths.get(getFontsDir() + "Arvo-Bold.ttf")), 0, CACHE_KEY_2)
                 }, inputStream);
     }

     Assert.assertEquals(parsedFonts.getFontsSources().length, loadedCache.getFontsSources().length);
 }

 /// 
 /// Load the font data only when required instead of storing it in the memory
 /// for the entire lifetime of the "FontSettings" object.
 /// 
 private static class SearchCacheStream extends StreamFontSource
 {
     public SearchCacheStream(String cacheKey)
     {
         super(0, cacheKey);

     }

     public FileInputStream openFontDataStream() throws Exception
     {
         return new FileInputStream(getFontsDir() + "Arvo-Regular.ttf");
     }
 }
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getCacheKeyInternal() {#getCacheKeyInternal}
```
public String getCacheKeyInternal()
```




**Returns:**
java.lang.String
### getFilePath() {#getFilePath}
```
public String getFilePath()
```




**Returns:**
java.lang.String
### getFontBytes() {#getFontBytes}
```
public byte[] getFontBytes()
```




**Returns:**
byte[]
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
### getSize() {#getSize}
```
public int getSize()
```




**Returns:**
int
### getType() {#getType}
```
public int getType()
```


يرجع نوع مصدر الخط.

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
### isEmbedded() {#isEmbedded}
```
public boolean isEmbedded()
```




**Returns:**
boolean
### openFontDataStream() {#openFontDataStream}
```
public abstract InputStream openFontDataStream()
```


يجب أن تفتح هذه الطريقة التدفق ببيانات الخط عند الطلب.

 **Remarks:** 

سيتم إغلاق التدفق بعد القراءة. لا حاجة لإغلاقه صراحةً.

 **Examples:** 

يوضح كيفية تحميل الخطوط من التدفق.

```

 public void streamFontSourceFileRendering() throws Exception {
     FontSettings fontSettings = new FontSettings();
     fontSettings.setFontsSources(new FontSourceBase[]{new StreamFontSourceFile()});

     DocumentBuilder builder = new DocumentBuilder();
     builder.getDocument().setFontSettings(fontSettings);
     builder.getFont().setName("Kreon-Regular");
     builder.writeln("Test aspose text when saving to PDF.");

     builder.getDocument().save(getArtifactsDir() + "FontSettings.StreamFontSourceFileRendering.pdf");
 }

 /// 
 /// Load the font data only when required instead of storing it in the memory for the entire lifetime of the "FontSettings" object.
 /// 
 private static class StreamFontSourceFile extends StreamFontSource  {
     public FileInputStream openFontDataStream() throws Exception {
         return new FileInputStream(getFontsDir() + "Kreon-Regular.ttf");
     }
 }
 
```

**Returns:**
java.io.InputStream - تدفق بيانات الخط.
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

