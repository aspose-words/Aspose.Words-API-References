---
title: "StreamFontSource"
linktitle: "StreamFontSource"
second_title: "Aspose.Words für Java"
description: "Basisklasse für benutzerdefinierte Stream‑Font‑Quellen in Java."
type: docs
weight: 635
url: /de/java/com.aspose.words/streamfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public abstract class StreamFontSource extends FontSourceBase
```

Basisklasse für benutzerdefinierte Stream‑Schriftquellen.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Um die Stream‑Font‑Quelle zu verwenden, sollten Sie eine abgeleitete Klasse von [StreamFontSource](../../com.aspose.words/streamfontsource/) erstellen und eine Implementierung der Methode [openFontDataStream()](../../com.aspose.words/streamfontsource/\#openFontDataStream) bereitstellen.

[openFontDataStream()](../../com.aspose.words/streamfontsource/\#openFontDataStream) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](../../com.aspose.words/streamfontsource/) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../../com.aspose.words/fontsettings/) lifetime.

 **Examples:** 

Zeigt, wie Schriftarten aus einem Stream geladen werden.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Gibt die Liste der über diese Quelle verfügbaren Schriftarten zurück. |
| [getCacheKey()](#getCacheKey) | Der Schlüssel dieser Quelle im Cache. |
| [getCacheKeyInternal()](#getCacheKeyInternal) |  |
| [getFilePath()](#getFilePath) |  |
| [getFontBytes()](#getFontBytes) |  |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Gibt die Priorität der Schriftquellen zurück. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getSize()](#getSize) |  |
| [getType()](#getType) | Gibt den Typ der Schriftquelle zurück. |
| [getWarningCallback()](#getWarningCallback) | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte. |
| [isEmbedded()](#isEmbedded) |  |
| [openFontDataStream()](#openFontDataStream) | Diese Methode sollte den Stream mit den Schriftartdaten bei Bedarf öffnen. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formattreue führen könnte. |
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


Gibt den Typ der Schriftquelle zurück.

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


Diese Methode sollte den Stream mit den Schriftartdaten bei Bedarf öffnen.

 **Remarks:** 

Der Stream wird nach dem Lesen geschlossen. Es ist nicht erforderlich, ihn explizit zu schließen.

 **Examples:** 

Zeigt, wie Schriftarten aus einem Stream geladen werden.

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
java.io.InputStream - Schriftartdaten‑Stream.
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

