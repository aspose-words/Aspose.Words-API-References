---
title: "FontFallbackSettings"
linktitle: "FontFallbackSettings"
second_title: "Aspose.Words para Java"
description: "Especifica la configuración del mecanismo de reserva de fuentes en Java."
type: docs
weight: 323
url: /es/java/com.aspose.words/fontfallbacksettings/
---

**Inheritance:**
java.lang.Object
```
public class FontFallbackSettings
```

Especifica la configuración del mecanismo de respaldo de fuentes.

Para obtener más información, visite el artículo de documentación [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Por defecto, la configuración de reserva se inicializa con ajustes predefinidos que imitan la reserva de Microsoft Word.

 **Examples:** 

Muestra cómo distribuir fuentes de reserva a través de los rangos de códigos de caracteres Unicode.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [buildAutomatic()](#buildAutomatic) | Construye automáticamente la configuración de reserva escaneando las fuentes disponibles. |
| [load(InputStream stream)](#load-java.io.InputStream) |  |
| [load(String fileName)](#load-java.lang.String) | Carga la configuración de reserva de fuentes desde un archivo XML. |
| [loadMsOfficeFallbackSettings()](#loadMsOfficeFallbackSettings) | Carga la configuración de reserva predefinida que imita la reserva de Microsoft Word y utiliza fuentes de Microsoft Office. |
| [loadNotoFallbackSettings()](#loadNotoFallbackSettings) | Carga la configuración de reserva predefinida que utiliza fuentes Google Noto. |
| [save(OutputStream outputStream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Guarda la configuración de reserva actual en un archivo. |
### buildAutomatic() {#buildAutomatic}
```
public void buildAutomatic()
```


Construye automáticamente la configuración de reserva escaneando las fuentes disponibles.

 **Remarks:** 

Este método puede producir configuraciones de reserva no óptimas. Las fuentes se verifican mediante los campos [ Unicode Character Range ][Unicode Character Range] y no por la presencia real de glifos. Además, los rangos Unicode se verifican individualmente y varios rangos relacionados con un solo idioma/guion pueden usar fuentes de reserva diferentes.

 **Examples:** 

Muestra cómo distribuir fuentes de reserva a través de los rangos de códigos de caracteres Unicode.

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

### load(InputStream stream) {#load-java.io.InputStream}
```
public void load(InputStream stream)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### load(String fileName) {#load-java.lang.String}
```
public void load(String fileName)
```


Carga la configuración de reserva de fuentes desde un archivo XML.

 **Examples:** 

Muestra cómo cargar y guardar la configuración de reserva de fuentes hacia/desde un documento XML en el sistema de archivos local.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Load an XML document that defines a set of font fallback settings.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getFallbackSettings().load(getMyDir() + "Font fallback rules.xml");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

 // Save our document's current font fallback settings as an XML document.
 doc.getFontSettings().getFallbackSettings().save(getArtifactsDir() + "FallbackSettings.xml");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | Nombre del archivo de entrada. |

### loadMsOfficeFallbackSettings() {#loadMsOfficeFallbackSettings}
```
public void loadMsOfficeFallbackSettings()
```


Carga la configuración de reserva predefinida que imita la reserva de Microsoft Word y utiliza fuentes de Microsoft Office.

 **Examples:** 

Muestra cómo cargar la configuración de fuentes de reserva predefinida.

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


Carga la configuración de reserva predefinida que utiliza fuentes Google Noto.

 **Examples:** 

Muestra cómo añadir configuraciones de reserva de fuentes predefinidas para fuentes Google Noto.

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

Muestra cómo cargar la configuración de fuentes de reserva predefinida.

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

### save(OutputStream outputStream) {#save-java.io.OutputStream}
```
public void save(OutputStream outputStream)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Guarda la configuración de reserva actual en un archivo.

 **Examples:** 

Muestra cómo cargar y guardar la configuración de reserva de fuentes hacia/desde un documento XML en el sistema de archivos local.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Load an XML document that defines a set of font fallback settings.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getFallbackSettings().load(getMyDir() + "Font fallback rules.xml");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

 // Save our document's current font fallback settings as an XML document.
 doc.getFontSettings().getFallbackSettings().save(getArtifactsDir() + "FallbackSettings.xml");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | Nombre del archivo de salida. |

