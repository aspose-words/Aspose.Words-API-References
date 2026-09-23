---
title: "MemoryFontSource"
linktitle: "MemoryFontSource"
second_title: "Aspose.Words für Java"
description: "Stellt die einzelne TrueType-Schriftdatei dar, die im Speicher in Java abgelegt ist."
type: docs
weight: 461
url: /de/java/com.aspose.words/memoryfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class MemoryFontSource extends FontSourceBase
```

Stellt die einzelne TrueType-Schriftdatei dar, die im Speicher gespeichert ist.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Fonts ][Working with Fonts].

 **Examples:** 

Zeigt, wie ein Byte-Array mit Daten aus einer Schriftdatei als Schriftquelle verwendet wird.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [MemoryFontSource(byte[] fontData)](#MemoryFontSource-byte) | Konstruktor. |
| [MemoryFontSource(byte[] fontData, int priority)](#MemoryFontSource-byte---int) | Konstruktor. |
| [MemoryFontSource(byte[] fontData, int priority, String cacheKey)](#MemoryFontSource-byte---int-java.lang.String) | Konstruktor. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Gibt die Liste der über diese Quelle verfügbaren Schriftarten zurück. |
| [getCacheKey()](#getCacheKey) | Der Schlüssel dieser Quelle im Cache. |
| [getFontData()](#getFontData) | Binäre Schriftartdaten. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Gibt die Priorität der Schriftquellen zurück. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getType()](#getType) | Gibt den Typ der Schriftquelle zurück. |
| [getWarningCallback()](#getWarningCallback) | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte. |
### MemoryFontSource(byte[] fontData) {#MemoryFontSource-byte}
```
public MemoryFontSource(byte[] fontData)
```


Konstruktor.

 **Examples:** 

Zeigt, wie ein Byte-Array mit Daten aus einer Schriftdatei als Schriftquelle verwendet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontData | byte[] | Binäre Schriftartdaten. |

### MemoryFontSource(byte[] fontData, int priority) {#MemoryFontSource-byte---int}
```
public MemoryFontSource(byte[] fontData, int priority)
```


Konstruktor.

 **Examples:** 

Zeigt, wie ein Byte-Array mit Daten aus einer Schriftdatei als Schriftquelle verwendet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontData | byte[] | Binäre Schriftartdaten. |
| priority | int | Priorität der Schriftquelle. Siehe die Beschreibung der Eigenschaft [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) für weitere Informationen. |

### MemoryFontSource(byte[] fontData, int priority, String cacheKey) {#MemoryFontSource-byte---int-java.lang.String}
```
public MemoryFontSource(byte[] fontData, int priority, String cacheKey)
```


Konstruktor.

 **Examples:** 

Zeigt, wie der Initialisierungsprozess des Schrift-Cache beschleunigt werden kann.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontData | byte[] | Binäre Schriftartdaten. |
| priority | int | Priorität der Schriftquelle. Siehe die Beschreibung der Eigenschaft [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) für weitere Informationen. |
| cacheKey | java.lang.String | Der Schlüssel dieser Quelle im Cache. Siehe die Beschreibung der Eigenschaft [getCacheKey()](../../com.aspose.words/memoryfontsource/\#getCacheKey) für weitere Informationen. |

### getAvailableFonts() {#getAvailableFonts}
```
public ArrayList getAvailableFonts()
```


Gibt die Liste der über diese Quelle verfügbaren Schriftarten zurück.

 **Examples:** 

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

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


Der Schlüssel dieser Quelle im Cache.

 **Remarks:** 

Dieser Schlüssel wird verwendet, um Cache-Elemente beim Speichern/Laden des Schrift-Such-Cache mit  und  Methoden zu identifizieren.

 **Examples:** 

Zeigt, wie der Initialisierungsprozess des Schrift-Cache beschleunigt werden kann.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getFontData() {#getFontData}
```
public byte[] getFontData()
```


Binäre Schriftartdaten.

 **Examples:** 

Zeigt, wie ein Byte-Array mit Daten aus einer Schriftdatei als Schriftquelle verwendet wird.

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
byte[] - Der entsprechende byte[]-Wert.
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


Gibt die Priorität der Schriftquellen zurück.

 **Remarks:** 

Dieser Wert wird verwendet, wenn Schriftarten mit demselben Familiennamen und Stil in verschiedenen Schriftquellen vorhanden sind. In diesem Fall wählt Aspose.Words die Schriftart aus der Quelle mit dem höheren Prioritätswert aus.

Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie eine Schriftdatei im lokalen Dateisystem als Schriftquelle verwendet wird.

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
int – Die Priorität der Schriftquelle.
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


Gibt den Typ der Schriftquelle zurück.

 **Examples:** 

Zeigt, wie ein Byte-Array mit Daten aus einer Schriftdatei als Schriftquelle verwendet wird.

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
int – Der Typ der Schriftquelle. Der zurückgegebene Wert ist einer der Konstanten von [FontSourceType](../../com.aspose.words/fontsourcetype/).
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte.

 **Examples:** 

Zeigt, wie der Warn-Callback aufgerufen wird, wenn die Schriftquellen verwendet werden.

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


Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte.

 **Examples:** 

Zeigt, wie der Warn-Callback aufgerufen wird, wenn die Schriftquellen verwendet werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Der entsprechende [IWarningCallback](../../com.aspose.words/iwarningcallback/) Wert. |

