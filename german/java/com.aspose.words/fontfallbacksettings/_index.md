---
title: "FontFallbackSettings"
linktitle: "FontFallbackSettings"
second_title: "Aspose.Words für Java"
description: "Gibt die Einstellungen für den Schriftart‑Fallback‑Mechanismus in Java an."
type: docs
weight: 323
url: /de/java/com.aspose.words/fontfallbacksettings/
---

**Inheritance:**
java.lang.Object
```
public class FontFallbackSettings
```

Gibt die Einstellungen für den Schriftfallback‑Mechanismus an.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Standardmäßig werden die Fallback‑Einstellungen mit vordefinierten Werten initialisiert, die den Microsoft‑Word‑Fallback nachahmen.

 **Examples:** 

Zeigt, wie man Fallback‑Schriftarten über Unicode‑Zeichencodierungsbereiche verteilt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [buildAutomatic()](#buildAutomatic) | Erstellt automatisch die Fallback-Einstellungen, indem verfügbare Schriftarten gescannt werden. |
| [load(InputStream stream)](#load-java.io.InputStream) |  |
| [load(String fileName)](#load-java.lang.String) | Lädt die Schriftart-Fallback-Einstellungen aus einer XML-Datei. |
| [loadMsOfficeFallbackSettings()](#loadMsOfficeFallbackSettings) | Lädt vordefinierte Fallback-Einstellungen, die das Microsoft‑Word‑Fallback nachahmen und Microsoft‑Office‑Schriftarten verwenden. |
| [loadNotoFallbackSettings()](#loadNotoFallbackSettings) | Lädt vordefinierte Fallback-Einstellungen, die Google‑Noto‑Schriftarten verwenden. |
| [save(OutputStream outputStream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Speichert die aktuellen Fallback-Einstellungen in einer Datei. |
### buildAutomatic() {#buildAutomatic}
```
public void buildAutomatic()
```


Erstellt automatisch die Fallback-Einstellungen, indem verfügbare Schriftarten gescannt werden.

 **Remarks:** 

Diese Methode kann nicht optimale Fallback-Einstellungen erzeugen. Schriftarten werden anhand der [ Unicode Character Range ][Unicode Character Range] Felder geprüft und nicht anhand der tatsächlichen Glyphen‑Vorhandensein. Außerdem werden Unicode‑Bereiche einzeln geprüft und mehrere Bereiche, die zu einer einzelnen Sprache/Schrift gehören, können unterschiedliche Fallback‑Schriftarten verwenden.

 **Examples:** 

Zeigt, wie man Fallback‑Schriftarten über Unicode‑Zeichencodierungsbereiche verteilt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### load(String fileName) {#load-java.lang.String}
```
public void load(String fileName)
```


Lädt die Schriftart-Fallback-Einstellungen aus einer XML-Datei.

 **Examples:** 

Zeigt, wie man Schriftart‑Fallback‑Einstellungen aus einem XML-Dokument im lokalen Dateisystem lädt und speichert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Eingabedateiname. |

### loadMsOfficeFallbackSettings() {#loadMsOfficeFallbackSettings}
```
public void loadMsOfficeFallbackSettings()
```


Lädt vordefinierte Fallback-Einstellungen, die das Microsoft‑Word‑Fallback nachahmen und Microsoft‑Office‑Schriftarten verwenden.

 **Examples:** 

Zeigt, wie vordefinierte Fallback‑Schriftarteinstellungen geladen werden.

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


Lädt vordefinierte Fallback-Einstellungen, die Google‑Noto‑Schriftarten verwenden.

 **Examples:** 

Zeigt, wie vordefinierte Fallback‑Schriftarteinstellungen für Google‑Noto‑Schriftarten hinzugefügt werden.

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

Zeigt, wie vordefinierte Fallback‑Schriftarteinstellungen geladen werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Speichert die aktuellen Fallback-Einstellungen in einer Datei.

 **Examples:** 

Zeigt, wie man Schriftart‑Fallback‑Einstellungen aus einem XML-Dokument im lokalen Dateisystem lädt und speichert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Ausgabedateiname. |

