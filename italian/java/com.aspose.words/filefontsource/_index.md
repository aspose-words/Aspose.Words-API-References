---
title: "FileFontSource"
linktitle: "FileFontSource"
second_title: "Aspose.Words per Java"
description: "Rappresenta il singolo file di font TrueType memorizzato nel file system in Java."
type: docs
weight: 308
url: /it/java/com.aspose.words/filefontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class FileFontSource extends FontSourceBase
```

Rappresenta il singolo file di font TrueType memorizzato nel file system.

Per saperne di più, visita l'articolo di documentazione [ Working with Fonts ][Working with Fonts].

 **Examples:** 

Mostra come utilizzare un file di carattere nel file system locale come sorgente di caratteri.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [FileFontSource(String filePath)](#FileFontSource-java.lang.String) | Ctor. |
| [FileFontSource(String filePath, int priority)](#FileFontSource-java.lang.String-int) | Ctor. |
| [FileFontSource(String filePath, int priority, String cacheKey)](#FileFontSource-java.lang.String-int-java.lang.String) | Ctor. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Restituisce l'elenco dei caratteri disponibili tramite questa sorgente. |
| [getCacheKey()](#getCacheKey) | La chiave di questa origine nella cache. |
| [getFilePath()](#getFilePath) | Percorso al file del font. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Restituisce la priorità della sorgente di caratteri. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getType()](#getType) | Restituisce il tipo della sorgente di caratteri. |
| [getWarningCallback()](#getWarningCallback) | Chiamato durante l'elaborazione della sorgente di caratteri quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà del formato. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Chiamato durante l'elaborazione della sorgente di caratteri quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà del formato. |
### FileFontSource(String filePath) {#FileFontSource-java.lang.String}
```
public FileFontSource(String filePath)
```


Ctor.

 **Examples:** 

Mostra come utilizzare un file di carattere nel file system locale come sorgente di caratteri.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| filePath | java.lang.String | Percorso al file del font. |

### FileFontSource(String filePath, int priority) {#FileFontSource-java.lang.String-int}
```
public FileFontSource(String filePath, int priority)
```


Ctor.

 **Examples:** 

Mostra come utilizzare un file di carattere nel file system locale come sorgente di caratteri.

```

 FileFontSource fileFontSource = new FileFontSource(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", 0);

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{fileFontSource});

 Assert.assertEquals(getMyDir() + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.getFilePath());
 Assert.assertEquals(FontSourceType.FONT_FILE, fileFontSource.getType());
 Assert.assertEquals(0, fileFontSource.getPriority());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| filePath | java.lang.String | Percorso al file del font. |
| priority | int | Priorità della sorgente di caratteri. Vedi la descrizione della proprietà [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) per ulteriori informazioni. |

### FileFontSource(String filePath, int priority, String cacheKey) {#FileFontSource-java.lang.String-int-java.lang.String}
```
public FileFontSource(String filePath, int priority, String cacheKey)
```


Ctor.

 **Examples:** 

Mostra come velocizzare il processo di inizializzazione della cache dei font.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| filePath | java.lang.String | Percorso al file del font. |
| priority | int | Priorità della sorgente di caratteri. Vedi la descrizione della proprietà [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) per ulteriori informazioni. |
| cacheKey | java.lang.String | La chiave di questa origine nella cache. Vedi la descrizione della proprietà [getCacheKey()](../../com.aspose.words/filefontsource/\#getCacheKey) per ulteriori informazioni. |

### getAvailableFonts() {#getAvailableFonts}
```
public ArrayList getAvailableFonts()
```


Restituisce l'elenco dei caratteri disponibili tramite questa sorgente.

 **Examples:** 

Mostra come elencare i caratteri disponibili.

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


La chiave di questa origine nella cache.

 **Remarks:** 

Questa chiave è usata per identificare l'elemento della cache durante il salvataggio/caricamento della cache di ricerca dei font con i metodi  e .

Se la chiave non è specificata, allora [getFilePath()](../../com.aspose.words/filefontsource/\#getFilePath) verrà usata come chiave al suo posto.

 **Examples:** 

Mostra come velocizzare il processo di inizializzazione della cache dei font.

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
java.lang.String - Il valore java.lang.String corrispondente.
### getFilePath() {#getFilePath}
```
public String getFilePath()
```


Percorso al file del font.

 **Examples:** 

Mostra come utilizzare un file di carattere nel file system locale come sorgente di caratteri.

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
java.lang.String - Il valore java.lang.String corrispondente.
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


Restituisce la priorità della sorgente di caratteri.

 **Remarks:** 

Questo valore viene utilizzato quando ci sono caratteri con lo stesso nome di famiglia e stile in diverse sorgenti di caratteri. In questo caso Aspose.Words seleziona il carattere dalla sorgente con il valore di priorità più alto.

Il valore predefinito è 0.

 **Examples:** 

Mostra come utilizzare un file di carattere nel file system locale come sorgente di caratteri.

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
int - La priorità della sorgente di caratteri.
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


Restituisce il tipo della sorgente di caratteri.

 **Examples:** 

Mostra come utilizzare un file di carattere nel file system locale come sorgente di caratteri.

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
int - Il tipo della sorgente di caratteri. Il valore restituito è una delle costanti [FontSourceType](../../com.aspose.words/fontsourcetype/).
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Chiamato durante l'elaborazione della sorgente di caratteri quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà del formato.

 **Examples:** 

Mostra come chiamare la callback di avviso quando si lavora con le sorgenti di caratteri.

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


Chiamato durante l'elaborazione della sorgente di caratteri quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà del formato.

 **Examples:** 

Mostra come chiamare la callback di avviso quando si lavora con le sorgenti di caratteri.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Il valore corrispondente di [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

