---
title: "StreamFontSource"
linktitle: "StreamFontSource"
second_title: "Aspose.Words para Java"
description: "Clase base para la fuente de fuente de flujo definida por el usuario en Java."
type: docs
weight: 635
url: /es/java/com.aspose.words/streamfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public abstract class StreamFontSource extends FontSourceBase
```

Clase base para la fuente de fuente de flujo definida por el usuario.

Para obtener más información, visite el artículo de documentación [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Para usar la fuente de fuente de flujo, debe crear una clase derivada de [StreamFontSource](../../com.aspose.words/streamfontsource/) y proporcionar la implementación del método [openFontDataStream()](../../com.aspose.words/streamfontsource/\#openFontDataStream).

[openFontDataStream()](../../com.aspose.words/streamfontsource/\#openFontDataStream) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](../../com.aspose.words/streamfontsource/) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../../com.aspose.words/fontsettings/) lifetime.

 **Examples:** 

Muestra cómo cargar fuentes desde un flujo.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Devuelve la lista de fuentes disponibles a través de esta fuente. |
| [getCacheKey()](#getCacheKey) | La clave de esta fuente en la caché. |
| [getCacheKeyInternal()](#getCacheKeyInternal) |  |
| [getFilePath()](#getFilePath) |  |
| [getFontBytes()](#getFontBytes) |  |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Devuelve la prioridad de la fuente de fuentes. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getSize()](#getSize) |  |
| [getType()](#getType) | Devuelve el tipo de la fuente de fuentes. |
| [getWarningCallback()](#getWarningCallback) | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| [isEmbedded()](#isEmbedded) |  |
| [openFontDataStream()](#openFontDataStream) | Este método debe abrir el flujo con los datos de la fuente bajo demanda. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
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


Devuelve el tipo de la fuente de fuentes.

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


Este método debe abrir el flujo con los datos de la fuente bajo demanda.

 **Remarks:** 

El flujo se cerrará después de la lectura. No es necesario cerrarlo explícitamente.

 **Examples:** 

Muestra cómo cargar fuentes desde un flujo.

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
java.io.InputStream - Flujo de datos de la fuente.
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

