---
title: StreamFontSource
linktitle: StreamFontSource
second_title: Aspose.Words for Java
description: Base class for user-defined stream font source in Java.
type: docs
weight: 608
url: /java/com.aspose.words/streamfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public abstract class StreamFontSource extends FontSourceBase
```

Base class for user-defined stream font source.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.

 **Remarks:** 

In order to use the stream font source you should create a derived class from the [StreamFontSource](../../com.aspose.words/streamfontsource/) and provide implementation of the [openFontDataStream()](../../com.aspose.words/streamfontsource/\#openFontDataStream) method.

[openFontDataStream()](../../com.aspose.words/streamfontsource/\#openFontDataStream) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](../../com.aspose.words/streamfontsource/) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../../com.aspose.words/fontsettings/) lifetime.

 **Examples:** 

Shows how to load fonts from stream.

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
## Methods

| Method | Description |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Returns list of fonts available via this source. |
| [getCacheKey()](#getCacheKey) | The key of this source in the cache. |
| [getCacheKeyInternal()](#getCacheKeyInternal) |  |
| [getFilePath()](#getFilePath) |  |
| [getFontBytes()](#getFontBytes) |  |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Returns the font source priority. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getSize()](#getSize) |  |
| [getType()](#getType) | Returns the type of the font source. |
| [getWarningCallback()](#getWarningCallback) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [openFontDataStream()](#openFontDataStream) | This method should open the stream with font data on demand. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
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


Returns the type of the font source.

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
### openFontDataStream() {#openFontDataStream}
```
public abstract InputStream openFontDataStream()
```


This method should open the stream with font data on demand.

 **Remarks:** 

The stream will be closed after reading. There is no need to close it explicitly.

 **Examples:** 

Shows how to load fonts from stream.

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
java.io.InputStream - Font data stream.
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

