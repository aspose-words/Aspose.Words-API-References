---
title: FolderFontSource
linktitle: FolderFontSource
second_title: Aspose.Words for Java
description: Represents the folder that contains TrueType font files in Java.
type: docs
weight: 311
url: /java/com.aspose.words/folderfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class FolderFontSource extends FontSourceBase
```

Represents the folder that contains TrueType font files.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.

 **Examples:** 

Shows how to use a local system folder which contains fonts as a font source.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [FolderFontSource(String folderPath, boolean scanSubfolders)](#FolderFontSource-java.lang.String-boolean) | Ctor. |
| [FolderFontSource(String folderPath, boolean scanSubfolders, int priority)](#FolderFontSource-java.lang.String-boolean-int) | Ctor. |
## Methods

| Method | Description |
| --- | --- |
| [getAvailableFonts()](#getAvailableFonts) | Returns list of fonts available via this source. |
| [getFolderPath()](#getFolderPath) | Path to the folder. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Returns the font source priority. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getScanSubfolders()](#getScanSubfolders) | Determines whether or not to scan the subfolders. |
| [getType()](#getType) | Returns the type of the font source. |
| [getWarningCallback()](#getWarningCallback) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
### FolderFontSource(String folderPath, boolean scanSubfolders) {#FolderFontSource-java.lang.String-boolean}
```
public FolderFontSource(String folderPath, boolean scanSubfolders)
```


Ctor.

 **Examples:** 

Shows how to use a local system folder which contains fonts as a font source.

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
| Parameter | Type | Description |
| --- | --- | --- |
| folderPath | java.lang.String | Path to folder. |
| scanSubfolders | boolean | Determines whether or not to scan subfolders. |

### FolderFontSource(String folderPath, boolean scanSubfolders, int priority) {#FolderFontSource-java.lang.String-boolean-int}
```
public FolderFontSource(String folderPath, boolean scanSubfolders, int priority)
```


Ctor.

 **Examples:** 

Shows how to use a local system folder which contains fonts as a font source.

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
| Parameter | Type | Description |
| --- | --- | --- |
| folderPath | java.lang.String | Path to folder. |
| scanSubfolders | boolean | Determines whether or not to scan subfolders. |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) property description for more information. |

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
### getFolderPath() {#getFolderPath}
```
public String getFolderPath()
```


Path to the folder.

 **Examples:** 

Shows how to use a local system folder which contains fonts as a font source.

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
java.lang.String - The corresponding java.lang.String value.
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
### getScanSubfolders() {#getScanSubfolders}
```
public boolean getScanSubfolders()
```


Determines whether or not to scan the subfolders.

 **Examples:** 

Shows how to use a local system folder which contains fonts as a font source.

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
boolean - The corresponding  boolean  value.
### getType() {#getType}
```
public int getType()
```


Returns the type of the font source.

 **Examples:** 

Shows how to use a local system folder which contains fonts as a font source.

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

