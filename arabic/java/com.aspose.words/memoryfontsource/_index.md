---
title: "MemoryFontSource"
linktitle: "MemoryFontSource"
second_title: "Aspose.Words لـ Java"
description: "يمثل ملف TrueType الخط الفردي المخزن في الذاكرة في Java."
type: docs
weight: 461
url: /ar/java/com.aspose.words/memoryfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class MemoryFontSource extends FontSourceBase
```

يمثل ملف خط TrueType الفردي المخزن في الذاكرة.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fonts ][Working with Fonts].

 **Examples:** 

يوضح كيفية استخدام مصفوفة بايت تحتوي على بيانات من ملف خط كمصدر للخط.

```

 byte[] fontBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf"));
 MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{memoryFontSource});

 Assert.assertEquals(FontSourceType.MEMORY_FONT, memoryFontSource.getType());
 Assert.assertEquals(0, memoryFontSource.getPriority());
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [MemoryFontSource(byte[] fontData)](#MemoryFontSource-byte) | المُنشئ. |
| [MemoryFontSource(byte[] fontData, int priority)](#MemoryFontSource-byte---int) | المُنشئ. |
| [MemoryFontSource(byte[] fontData, int priority, String cacheKey)](#MemoryFontSource-byte---int-java.lang.String) | المُنشئ. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | يرجع قائمة الخطوط المتاحة عبر هذا المصدر. |
| [getCacheKey()](#getCacheKey) | المفتاح لهذا المصدر في الذاكرة المؤقتة. |
| [getFontData()](#getFontData) | بيانات خط ثنائية. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | يرجع أولوية مصدر الخط. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getType()](#getType) | يرجع نوع مصدر الخط. |
| [getWarningCallback()](#getWarningCallback) | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | يُستدعى أثناء معالجة مصدر الخط عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |
### MemoryFontSource(byte[] fontData) {#MemoryFontSource-byte}
```
public MemoryFontSource(byte[] fontData)
```


المُنشئ.

 **Examples:** 

يوضح كيفية استخدام مصفوفة بايت تحتوي على بيانات من ملف خط كمصدر للخط.

```

 byte[] fontBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf"));
 MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{memoryFontSource});

 Assert.assertEquals(FontSourceType.MEMORY_FONT, memoryFontSource.getType());
 Assert.assertEquals(0, memoryFontSource.getPriority());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontData | byte[] | بيانات خط ثنائية. |

### MemoryFontSource(byte[] fontData, int priority) {#MemoryFontSource-byte---int}
```
public MemoryFontSource(byte[] fontData, int priority)
```


المُنشئ.

 **Examples:** 

يوضح كيفية استخدام مصفوفة بايت تحتوي على بيانات من ملف خط كمصدر للخط.

```

 byte[] fontBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf"));
 MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{memoryFontSource});

 Assert.assertEquals(FontSourceType.MEMORY_FONT, memoryFontSource.getType());
 Assert.assertEquals(0, memoryFontSource.getPriority());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontData | byte[] | بيانات خط ثنائية. |
| priority | int | أولوية مصدر الخط. راجع وصف الخاصية [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) لمزيد من المعلومات. |

### MemoryFontSource(byte[] fontData, int priority, String cacheKey) {#MemoryFontSource-byte---int-java.lang.String}
```
public MemoryFontSource(byte[] fontData, int priority, String cacheKey)
```


المُنشئ.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontData | byte[] | بيانات خط ثنائية. |
| priority | int | أولوية مصدر الخط. راجع وصف الخاصية [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) لمزيد من المعلومات. |
| cacheKey | java.lang.String | المفتاح لهذا المصدر في الذاكرة المؤقتة. راجع وصف الخاصية [getCacheKey()](../../com.aspose.words/memoryfontsource/\#getCacheKey) لمزيد من المعلومات. |

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
### getFontData() {#getFontData}
```
public byte[] getFontData()
```


بيانات خط ثنائية.

 **Examples:** 

يوضح كيفية استخدام مصفوفة بايت تحتوي على بيانات من ملف خط كمصدر للخط.

```

 byte[] fontBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf"));
 MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{memoryFontSource});

 Assert.assertEquals(FontSourceType.MEMORY_FONT, memoryFontSource.getType());
 Assert.assertEquals(0, memoryFontSource.getPriority());
 
```

**Returns:**
byte[] - القيمة المقابلة من نوع byte[] .
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
### getType() {#getType}
```
public int getType()
```


يرجع نوع مصدر الخط.

 **Examples:** 

يوضح كيفية استخدام مصفوفة بايت تحتوي على بيانات من ملف خط كمصدر للخط.

```

 byte[] fontBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf"));
 MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{memoryFontSource});

 Assert.assertEquals(FontSourceType.MEMORY_FONT, memoryFontSource.getType());
 Assert.assertEquals(0, memoryFontSource.getPriority());
 
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

