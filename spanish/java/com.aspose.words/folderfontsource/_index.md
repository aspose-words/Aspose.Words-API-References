---
title: "FolderFontSource"
linktitle: "FolderFontSource"
second_title: "Aspose.Words para Java"
description: "Representa la carpeta que contiene archivos de fuentes TrueType en Java."
type: docs
weight: 318
url: /es/java/com.aspose.words/folderfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class FolderFontSource extends FontSourceBase
```

Representa la carpeta que contiene archivos de fuentes TrueType.

Para obtener más información, visite el artículo de documentación [ Working with Fonts ][Working with Fonts].

 **Examples:** 

Muestra cómo usar una carpeta local del sistema que contiene fuentes como una fuente de fuentes.

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [FolderFontSource(String folderPath, boolean scanSubfolders)](#FolderFontSource-java.lang.String-boolean) | Ctor. |
| [FolderFontSource(String folderPath, boolean scanSubfolders, int priority)](#FolderFontSource-java.lang.String-boolean-int) | Ctor. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Devuelve la lista de fuentes disponibles a través de esta fuente. |
| [getFolderPath()](#getFolderPath) | Ruta a la carpeta. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Devuelve la prioridad de la fuente de fuentes. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getScanSubfolders()](#getScanSubfolders) | Determina si se deben escanear o no las subcarpetas. |
| [getType()](#getType) | Devuelve el tipo de la fuente de fuentes. |
| [getWarningCallback()](#getWarningCallback) | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
### FolderFontSource(String folderPath, boolean scanSubfolders) {#FolderFontSource-java.lang.String-boolean}
```
public FolderFontSource(String folderPath, boolean scanSubfolders)
```


Ctor.

 **Examples:** 

Muestra cómo usar una carpeta local del sistema que contiene fuentes como una fuente de fuentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| folderPath | java.lang.String | Ruta a la carpeta. |
| scanSubfolders | boolean | Determina si se deben escanear o no las subcarpetas. |

### FolderFontSource(String folderPath, boolean scanSubfolders, int priority) {#FolderFontSource-java.lang.String-boolean-int}
```
public FolderFontSource(String folderPath, boolean scanSubfolders, int priority)
```


Ctor.

 **Examples:** 

Muestra cómo usar una carpeta local del sistema que contiene fuentes como una fuente de fuentes.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| folderPath | java.lang.String | Ruta a la carpeta. |
| scanSubfolders | boolean | Determina si se deben escanear o no las subcarpetas. |
| priority | int | Prioridad de la fuente de fuentes. Consulte la descripción de la propiedad [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) para obtener más información. |

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
### getFolderPath() {#getFolderPath}
```
public String getFolderPath()
```


Ruta a la carpeta.

 **Examples:** 

Muestra cómo usar una carpeta local del sistema que contiene fuentes como una fuente de fuentes.

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
### getScanSubfolders() {#getScanSubfolders}
```
public boolean getScanSubfolders()
```


Determina si se deben escanear o no las subcarpetas.

 **Examples:** 

Muestra cómo usar una carpeta local del sistema que contiene fuentes como una fuente de fuentes.

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
boolean - El valor  boolean  correspondiente.
### getType() {#getType}
```
public int getType()
```


Devuelve el tipo de la fuente de fuentes.

 **Examples:** 

Muestra cómo usar una carpeta local del sistema que contiene fuentes como una fuente de fuentes.

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

