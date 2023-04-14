---
title: FontFallbackSettings
linktitle: FontFallbackSettings
second_title: Aspose.Words for Java API Reference
description: Specifies font fallback mechanism settings in Java.
type: docs
weight: 280
url: /java/com.aspose.words/fontfallbacksettings/
---

**Inheritance:**
java.lang.Object
```
public class FontFallbackSettings
```

Specifies font fallback mechanism settings.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.

 **Remarks:** 

By default fallback settings are initialized with predefined settings which mimics the Microsoft Word fallback.

 **Examples:** 

Shows how to distribute fallback fonts across Unicode character code ranges.

```

 Document doc = new Document();

 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);
 FontFallbackSettings fontFallbackSettings = fontSettings.getFallbackSettings();

 // Configure our font settings to source fonts only from the "MyFonts" folder.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false);
 fontSettings.setFontsSources(new FontSourceBase[]{folderFontSource});

 // Calling the "BuildAutomatic" method will generate a fallback scheme that
 // distributes accessible fonts across as many Unicode character codes as possible.
 // In our case, it only has access to the handful of fonts inside the "MyFonts" folder.
 fontFallbackSettings.buildAutomatic();
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

 // We can also load a custom substitution scheme from a file like this.
 // This scheme applies the "AllegroOpen" font across the "0000-00ff" Unicode blocks, the "AllegroOpen" font across "0100-024f",
 // and the "M+ 2m" font in all other ranges that other fonts in the scheme do not cover.
 fontFallbackSettings.load(getMyDir() + "Custom font fallback settings.xml");

 // Create a document builder and set its font to one that does not exist in any of our sources.
 // Our font settings will invoke the fallback scheme for characters that we type using the unavailable font.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Missing Font");

 // Use the builder to print every Unicode character from 0x0021 to 0x052F,
 // with descriptive lines dividing Unicode blocks we defined in our custom font fallback scheme.
 for (int i = 0x0021; i < 0x0530; i++) {
     switch (i) {
         case 0x0021:
             builder.writeln("\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
             break;
         case 0x0100:
             builder.writeln("\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
             break;
         case 0x0250:
             builder.writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
             break;
     }

     builder.write(MessageFormat.format("{0}", (char) i));
 }

 doc.save(getArtifactsDir() + "FontSettings.FallbackSettingsCustom.pdf");
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Methods

| Method | Description |
| --- | --- |
| [buildAutomatic()](#buildAutomatic) | Automatically builds the fallback settings by scanning available fonts. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [hashCode()](#hashCode) |  |
| [load(InputStream stream)](#load-java.io.InputStream) |  |
| [load(String fileName)](#load-java.lang.String) | Loads font fallback settings from XML file. |
| [loadMsOfficeFallbackSettings()](#loadMsOfficeFallbackSettings) | Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts. |
| [loadNotoFallbackSettings()](#loadNotoFallbackSettings) | Loads predefined fallback settings which uses Google Noto fonts. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [save(OutputStream outputStream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Saves the current fallback settings to file. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### buildAutomatic() {#buildAutomatic}
```
public void buildAutomatic()
```


Automatically builds the fallback settings by scanning available fonts.

 **Remarks:** 

This method may produce non-optimal fallback settings. Fonts are checked by [ Unicode Character Range ][Unicode Character Range] fields and not by the actual glyphs presence. Also Unicode ranges are checked individually and several ranges related to single language/script may use different fallback fonts.

 **Examples:** 

Shows how to distribute fallback fonts across Unicode character code ranges.

```

 Document doc = new Document();

 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);
 FontFallbackSettings fontFallbackSettings = fontSettings.getFallbackSettings();

 // Configure our font settings to source fonts only from the "MyFonts" folder.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false);
 fontSettings.setFontsSources(new FontSourceBase[]{folderFontSource});

 // Calling the "BuildAutomatic" method will generate a fallback scheme that
 // distributes accessible fonts across as many Unicode character codes as possible.
 // In our case, it only has access to the handful of fonts inside the "MyFonts" folder.
 fontFallbackSettings.buildAutomatic();
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

 // We can also load a custom substitution scheme from a file like this.
 // This scheme applies the "AllegroOpen" font across the "0000-00ff" Unicode blocks, the "AllegroOpen" font across "0100-024f",
 // and the "M+ 2m" font in all other ranges that other fonts in the scheme do not cover.
 fontFallbackSettings.load(getMyDir() + "Custom font fallback settings.xml");

 // Create a document builder and set its font to one that does not exist in any of our sources.
 // Our font settings will invoke the fallback scheme for characters that we type using the unavailable font.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Missing Font");

 // Use the builder to print every Unicode character from 0x0021 to 0x052F,
 // with descriptive lines dividing Unicode blocks we defined in our custom font fallback scheme.
 for (int i = 0x0021; i < 0x0530; i++) {
     switch (i) {
         case 0x0021:
             builder.writeln("\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
             break;
         case 0x0100:
             builder.writeln("\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
             break;
         case 0x0250:
             builder.writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
             break;
     }

     builder.write(MessageFormat.format("{0}", (char) i));
 }

 doc.save(getArtifactsDir() + "FontSettings.FallbackSettingsCustom.pdf");
 
```


[Unicode Character Range]: https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### load(InputStream stream) {#load-java.io.InputStream}
```
public void load(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### load(String fileName) {#load-java.lang.String}
```
public void load(String fileName)
```


Loads font fallback settings from XML file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Input file name.

 **Examples:** 

Shows how to load and save font fallback settings to/from an XML document in the local file system.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Load an XML document that defines a set of font fallback settings.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getFallbackSettings().load(getMyDir() + "Font fallback rules.xml");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

 // Save our document's current font fallback settings as an XML document.
 doc.getFontSettings().getFallbackSettings().save(getArtifactsDir() + "FallbackSettings.xml");
 
``` |

### loadMsOfficeFallbackSettings() {#loadMsOfficeFallbackSettings}
```
public void loadMsOfficeFallbackSettings()
```


Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts.

 **Examples:** 

Shows how to load pre-defined fallback font settings.

```

 Document doc = new Document();

 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);
 FontFallbackSettings fontFallbackSettings = fontSettings.getFallbackSettings();

 // Save the default fallback font scheme to an XML document.
 // For example, one of the elements has a value of "0C00-0C7F" for Range and a corresponding "Vani" value for FallbackFonts.
 // This means that if the font some text is using does not have symbols for the 0x0C00-0x0C7F Unicode block,
 // the fallback scheme will use symbols from the "Vani" font substitute.
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.Default.xml");

 // Below are two pre-defined font fallback schemes we can choose from.
 // 1 -  Use the default Microsoft Office scheme, which is the same one as the default:
 fontFallbackSettings.loadMsOfficeFallbackSettings();
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

 // 2 -  Use the scheme built from Google Noto fonts:
 fontFallbackSettings.loadNotoFallbackSettings();
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
 
```

### loadNotoFallbackSettings() {#loadNotoFallbackSettings}
```
public void loadNotoFallbackSettings()
```


Loads predefined fallback settings which uses Google Noto fonts.

 **Examples:** 

Shows how to add predefined font fallback settings for Google Noto fonts.

```

 FontSettings fontSettings = new FontSettings();

 // These are free fonts licensed under the SIL Open Font License.
 // We can download the fonts here:
 // https://www.google.com/get/noto/#sans-lgc
 fontSettings.setFontsFolder(getFontsDir() + "Noto", false);

 // Note that the predefined settings only use Sans-style Noto fonts with regular weight.
 // Some of the Noto fonts use advanced typography features.
 // Fonts featuring advanced typography may not be rendered correctly as Aspose.Words currently do not support them.
 fontSettings.getFallbackSettings().loadNotoFallbackSettings();
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(false);
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Noto Sans");

 Document doc = new Document();
 doc.setFontSettings(fontSettings);
 
```

Shows how to load pre-defined fallback font settings.

```

 Document doc = new Document();

 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);
 FontFallbackSettings fontFallbackSettings = fontSettings.getFallbackSettings();

 // Save the default fallback font scheme to an XML document.
 // For example, one of the elements has a value of "0C00-0C7F" for Range and a corresponding "Vani" value for FallbackFonts.
 // This means that if the font some text is using does not have symbols for the 0x0C00-0x0C7F Unicode block,
 // the fallback scheme will use symbols from the "Vani" font substitute.
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.Default.xml");

 // Below are two pre-defined font fallback schemes we can choose from.
 // 1 -  Use the default Microsoft Office scheme, which is the same one as the default:
 fontFallbackSettings.loadMsOfficeFallbackSettings();
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

 // 2 -  Use the scheme built from Google Noto fonts:
 fontFallbackSettings.loadNotoFallbackSettings();
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
 
```

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### save(OutputStream outputStream) {#save-java.io.OutputStream}
```
public void save(OutputStream outputStream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Saves the current fallback settings to file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Output file name.

 **Examples:** 

Shows how to load and save font fallback settings to/from an XML document in the local file system.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Load an XML document that defines a set of font fallback settings.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getFallbackSettings().load(getMyDir() + "Font fallback rules.xml");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

 // Save our document's current font fallback settings as an XML document.
 doc.getFontSettings().getFallbackSettings().save(getArtifactsDir() + "FallbackSettings.xml");
 
``` |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

