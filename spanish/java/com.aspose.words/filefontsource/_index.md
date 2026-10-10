---
title: "FileFontSource"
linktitle: "FileFontSource"
second_title: "Aspose.Words para Java"
description: "Representa el único archivo de fuente TrueType almacenado en el sistema de archivos en Java."
type: docs
weight: 308
url: /es/java/com.aspose.words/filefontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class FileFontSource extends FontSourceBase
```

Representa el único archivo de fuente TrueType almacenado en el sistema de archivos.

Para obtener más información, visite el artículo de documentación [ Working with Fonts ][Working with Fonts].

 **Examples:** 

Muestra cómo usar un archivo de fuente en el sistema de archivos local como una fuente de fuentes.

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [FileFontSource(String filePath)](#FileFontSource-java.lang.String) | Ctor. |
| [FileFontSource(String filePath, int priority)](#FileFontSource-java.lang.String-int) | Ctor. |
| [FileFontSource(String filePath, int priority, String cacheKey)](#FileFontSource-java.lang.String-int-java.lang.String) | Ctor. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Devuelve la lista de fuentes disponibles a través de esta fuente. |
| [getCacheKey()](#getCacheKey) | La clave de esta fuente en la caché. |
| [getFilePath()](#getFilePath) | Ruta al archivo de fuente. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Devuelve la prioridad de la fuente de fuentes. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getType()](#getType) | Devuelve el tipo de la fuente de fuentes. |
| [getWarningCallback()](#getWarningCallback) | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
### FileFontSource(String filePath) {#FileFontSource-java.lang.String}
```
public FileFontSource(String filePath)
```


Ctor.

 **Examples:** 

Muestra cómo usar un archivo de fuente en el sistema de archivos local como una fuente de fuentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| filePath | java.lang.String | Ruta al archivo de fuente. |

### FileFontSource(String filePath, int priority) {#FileFontSource-java.lang.String-int}
```
public FileFontSource(String filePath, int priority)
```


Ctor.

 **Examples:** 

Muestra cómo usar un archivo de fuente en el sistema de archivos local como una fuente de fuentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| filePath | java.lang.String | Ruta al archivo de fuente. |
| priority | int | Prioridad de la fuente de fuentes. Consulte la descripción de la propiedad [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) para obtener más información. |

### FileFontSource(String filePath, int priority, String cacheKey) {#FileFontSource-java.lang.String-int-java.lang.String}
```
public FileFontSource(String filePath, int priority, String cacheKey)
```


Ctor.

 **Examples:** 

Muestra cómo acelerar el proceso de inicialización de la caché de fuentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| filePath | java.lang.String | Ruta al archivo de fuente. |
| priority | int | Prioridad de la fuente de fuentes. Consulte la descripción de la propiedad [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) para obtener más información. |
| cacheKey | java.lang.String | La clave de esta fuente en la caché. Consulte la descripción de la propiedad [getCacheKey()](../../com.aspose.words/filefontsource/\#getCacheKey) para obtener más información. |

### getAvailableFonts() {#getAvailableFonts}
```
public ArrayList getAvailableFonts()
```


Devuelve la lista de fuentes disponibles a través de esta fuente.

 **Examples:** 

Muestra cómo enumerar las fuentes disponibles.

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


La clave de esta fuente en la caché.

 **Remarks:** 

Esta clave se usa para identificar el elemento de caché al guardar/cargar la caché de búsqueda de fuentes con los métodos  y .

Si no se especifica la clave, entonces [getFilePath()](../../com.aspose.words/filefontsource/\#getFilePath) se usará como clave.

 **Examples:** 

Muestra cómo acelerar el proceso de inicialización de la caché de fuentes.

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
java.lang.String - El valor java.lang.String correspondiente.
### getFilePath() {#getFilePath}
```
public String getFilePath()
```


Ruta al archivo de fuente.

 **Examples:** 

Muestra cómo usar un archivo de fuente en el sistema de archivos local como una fuente de fuentes.

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
java.lang.String - El valor java.lang.String correspondiente.
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


Devuelve la prioridad de la fuente de fuentes.

 **Remarks:** 

Este valor se usa cuando hay fuentes con el mismo nombre de familia y estilo en diferentes fuentes de fuentes. En este caso, Aspose.Words selecciona la fuente de la fuente con el valor de prioridad más alto.

El valor predeterminado es 0.

 **Examples:** 

Muestra cómo usar un archivo de fuente en el sistema de archivos local como una fuente de fuentes.

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
int - La prioridad de la fuente de fuentes.
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


Devuelve el tipo de la fuente de fuentes.

 **Examples:** 

Muestra cómo usar un archivo de fuente en el sistema de archivos local como una fuente de fuentes.

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
int - El tipo de la fuente de fuentes. El valor devuelto es una de las constantes [FontSourceType](../../com.aspose.words/fontsourcetype/).
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato.

 **Examples:** 

Muestra cómo llamar a la devolución de llamada de advertencia cuando se trabaja con las fuentes de fuentes.

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


Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato.

 **Examples:** 

Muestra cómo llamar a la devolución de llamada de advertencia cuando se trabaja con las fuentes de fuentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | El valor correspondiente de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

