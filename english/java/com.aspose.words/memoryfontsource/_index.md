---
title: MemoryFontSource
linktitle: MemoryFontSource
second_title: Aspose.Words for Java
description: Represents the single TrueType font file stored in memory in Java.
type: docs
weight: 440
url: /java/com.aspose.words/memoryfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class MemoryFontSource extends FontSourceBase
```

Represents the single TrueType font file stored in memory.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.

 **Examples:** 

Shows how to use a byte array with data from a font file as a font source.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [MemoryFontSource(byte[] fontData)](#MemoryFontSource-byte) | Ctor. |
| [MemoryFontSource(byte[] fontData, int priority)](#MemoryFontSource-byte---int) | Ctor. |
| [MemoryFontSource(byte[] fontData, int priority, String cacheKey)](#MemoryFontSource-byte---int-java.lang.String) | Ctor. |
## Methods

| Method | Description |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Returns list of fonts available via this source. |
| [getCacheKey()](#getCacheKey) | The key of this source in the cache. |
| [getFontData()](#getFontData) | Binary font data. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Returns the font source priority. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getType()](#getType) | Returns the type of the font source. |
| [getWarningCallback()](#getWarningCallback) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
### MemoryFontSource(byte[] fontData) {#MemoryFontSource-byte}
```
public MemoryFontSource(byte[] fontData)
```


Ctor.

 **Examples:** 

Shows how to use a byte array with data from a font file as a font source.

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
| Parameter | Type | Description |
| --- | --- | --- |
| fontData | byte[] | Binary font data. |

### MemoryFontSource(byte[] fontData, int priority) {#MemoryFontSource-byte---int}
```
public MemoryFontSource(byte[] fontData, int priority)
```


Ctor.

 **Examples:** 

Shows how to use a byte array with data from a font file as a font source.

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
| Parameter | Type | Description |
| --- | --- | --- |
| fontData | byte[] | Binary font data. |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) property description for more information. |

### MemoryFontSource(byte[] fontData, int priority, String cacheKey) {#MemoryFontSource-byte---int-java.lang.String}
```
public MemoryFontSource(byte[] fontData, int priority, String cacheKey)
```


Ctor.

 **Examples:** 

Shows how to speed up the font cache initialization process.

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
| Parameter | Type | Description |
| --- | --- | --- |
| fontData | byte[] | Binary font data. |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) property description for more information. |
| cacheKey | java.lang.String | The key of this source in the cache. See [getCacheKey()](../../com.aspose.words/memoryfontsource/\#getCacheKey) property description for more information. |

### getAvailableFonts() {#getAvailableFonts}
```
public ArrayList getAvailableFonts()
```


Returns list of fonts available via this source.

 **Examples:** 

Shows how to list available fonts.

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


The key of this source in the cache.

 **Remarks:** 

This key is used to identify cache item when saving/loading font search cache with  and  methods.

 **Examples:** 

Shows how to speed up the font cache initialization process.

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
java.lang.String - The corresponding java.lang.String value.
### getFontData() {#getFontData}
```
public byte[] getFontData()
```


Binary font data.

 **Examples:** 

Shows how to use a byte array with data from a font file as a font source.

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
byte[] - The corresponding byte[] value.
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


Returns the font source priority.

 **Remarks:** 

This value is used when there are fonts with the same family name and style in different font sources. In this case Aspose.Words selects the font from the source with the higher priority value.

The default value is 0.

 **Examples:** 

Shows how to use a font file in the local file system as a font source.

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
int - The font source priority.
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


Returns the type of the font source.

 **Examples:** 

Shows how to use a byte array with data from a font file as a font source.

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
int - The type of the font source. The returned value is one of [FontSourceType](../../com.aspose.words/fontsourcetype/) constants.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Called during processing of font source when an issue is detected that might result in formatting fidelity loss.

 **Examples:** 

Shows how to call warning callback when the font sources working with.

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


Called during processing of font source when an issue is detected that might result in formatting fidelity loss.

 **Examples:** 

Shows how to call warning callback when the font sources working with.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value. |

