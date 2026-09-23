---
title: "FontSettings"
linktitle: "FontSettings"
second_title: "Aspose.Words für Java"
description: "Gibt die Schriftarteinstellungen für ein Dokument in Java an."
type: docs
weight: 332
url: /de/java/com.aspose.words/fontsettings/
---

**Inheritance:**
java.lang.Object
```
public class FontSettings
```

Gibt die Schrift‑Einstellungen für ein Dokument an.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Aspose.Words verwendet Schriftarteinstellungen, um die Schriften im Dokument aufzulösen. Schriften werden hauptsächlich beim Erstellen des Dokumentlayouts oder beim Rendern in feste Seitenformate aufgelöst. Beim Laden einiger Formate kann Aspose.Words jedoch ebenfalls die Auflösung der Schriften benötigen. Beispielsweise kann Aspose.Words beim Laden von HTML-Dokumenten die Schriften auflösen, um eine Schriftfallback‑Funktion auszuführen. Daher wird empfohlen, die Schriftarteinstellungen beim Laden des Dokuments in [LoadOptions](../../com.aspose.words/loadoptions/) festzulegen. Oder zumindest vor dem Erstellen des Layouts oder dem Rendern des Dokuments in das feste Seitenformat.

Standardmäßig verwenden alle Dokumente eine einzige statische Instanz von Schriftarteinstellungen. Auf sie kann über die Eigenschaft [getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) zugegriffen werden.

Das Ändern der Schriftarteinstellungen ist jederzeit und von jedem Thread aus sicher. Es wird jedoch empfohlen, die Schriftarteinstellungen nicht zu ändern, während einige Dokumente verarbeitet werden, die diese Einstellungen verwenden. Dies kann dazu führen, dass dieselbe Schrift in verschiedenen Teilen des Dokuments unterschiedlich aufgelöst wird.

 **Examples:** 

Zeigt, wie ein Schriftquellen‑Verzeichnis festgelegt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arvo");
 builder.writeln("Hello world!");
 builder.getFont().setName("Amethysta");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 // Our font sources do not contain the font that we have used for text in this document.
 // If we use these font settings while rendering this document,
 // Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
 FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertEquals(1, originalFontSources.length);
 Assert.assertTrue(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));

 // The default font sources are missing the two fonts that we are using in this document.
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arvo")));
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));

 // Use the "SetFontsFolder" method to set a directory which will act as a new font source.
 // Pass "false" as the "recursive" argument to include fonts from all the font files that are in the directory
 // that we are passing in the first argument, but not include any fonts in any of that directory's subfolders.
 // Pass "true" as the "recursive" argument to include all font files in the directory that we are passing
 // in the first argument, as well as all the fonts in its subdirectories.
 FontSettings.getDefaultInstance().setFontsFolder(getFontsDir(), recursive);

 FontSourceBase[] newFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertEquals(1, newFontSources.length);
 Assert.assertFalse(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));
 Assert.assertTrue(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arvo")));

 // The "Amethysta" font is in a subfolder of the font directory.
 if (recursive) {
     Assert.assertEquals(30, newFontSources[0].getAvailableFonts().size());
     Assert.assertTrue(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 } else {
     Assert.assertEquals(18, newFontSources[0].getAvailableFonts().size());
     Assert.assertFalse(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 }

 doc.save(getArtifactsDir() + "FontSettings.SetFontsFolder.pdf");

 // Restore the original font sources.
 FontSettings.getDefaultInstance().setFontsSources(originalFontSources);
 
```

Zeigt, wie mehrere Schriftquellen‑Verzeichnisse festgelegt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Amethysta");
 builder.writeln("The quick brown fox jumps over the lazy dog.");
 builder.getFont().setName("Junction Light");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 // Our font sources do not contain the font that we have used for text in this document.
 // If we use these font settings while rendering this document,
 // Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
 FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertEquals(1, originalFontSources.length);
 Assert.assertTrue(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));

 // The default font sources are missing the two fonts that we are using in this document.
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Junction Light")));

 // Use the "SetFontsFolders" method to create a font source from each font directory that we pass as the first argument.
 // Pass "false" as the "recursive" argument to include fonts from all the font files that are in the directories
 // that we are passing in the first argument, but not include any fonts from any of the directories' subfolders.
 // Pass "true" as the "recursive" argument to include all font files in the directories that we are passing
 // in the first argument, as well as all the fonts in their subdirectories.
 FontSettings.getDefaultInstance().setFontsFolders(new String[]{getFontsDir() + "/Amethysta", getFontsDir() + "/Junction"}, recursive);

 FontSourceBase[] newFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertEquals(2, newFontSources.length);
 Assert.assertFalse(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));
 Assert.assertEquals(1, newFontSources[0].getAvailableFonts().size());
 Assert.assertTrue(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));

 // The "Junction" folder itself contains no font files, but has subfolders that do.
 if (recursive) {
     Assert.assertEquals(11, newFontSources[1].getAvailableFonts().size());
     Assert.assertTrue(IterableUtils.matchesAny(newFontSources[1].getAvailableFonts(), f -> f.getFullFontName().contains("Junction Light")));
 } else {
     Assert.assertEquals(0, newFontSources[1].getAvailableFonts().size());
 }

 doc.save(getArtifactsDir() + "FontSettings.SetFontsFolders.pdf");

 // Restore the original font sources.
 FontSettings.getDefaultInstance().setFontsSources(originalFontSources);
 
```

Zeigt, wie eine Schriftquelle zu unseren bestehenden Schriftquellen hinzugefügt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Amethysta");
 builder.writeln("The quick brown fox jumps over the lazy dog.");
 builder.getFont().setName("Junction Light");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertEquals(1, originalFontSources.length);

 Assert.assertTrue(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));

 // The default font source is missing two of the fonts that we are using in our document.
 // When we save this document, Aspose.Words will apply fallback fonts to all text formatted with inaccessible fonts.
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Junction Light")));

 // Create a font source from a folder that contains fonts.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), true);

 // Apply a new array of font sources that contains the original font sources, as well as our custom fonts.
 FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
 FontSettings.getDefaultInstance().setFontsSources(updatedFontSources);

 // Verify that Aspose.Words has access to all required fonts before we render the document to PDF.
 updatedFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertTrue(IterableUtils.matchesAny(updatedFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));
 Assert.assertTrue(IterableUtils.matchesAny(updatedFontSources[1].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 Assert.assertTrue(IterableUtils.matchesAny(updatedFontSources[1].getAvailableFonts(), f -> f.getFullFontName().contains("Junction Light")));

 doc.save(getArtifactsDir() + "FontSettings.AddFontSource.pdf");

 // Restore the original font sources.
 FontSettings.getDefaultInstance().setFontsSources(originalFontSources);
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [FontSettings()](#FontSettings) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getDefaultInstance()](#getDefaultInstance) | Statische Standard‑Schriftarteinstellungen. |
| [getFallbackSettings()](#getFallbackSettings) | Einstellungen zum Schrift‑Fallback‑Mechanismus. |
| [getFontsSources()](#getFontsSources) | Gibt eine Kopie des Arrays zurück, das die Liste der Quellen enthält, in denen Aspose.Words nach TrueType-Schriften sucht. |
| [getSubstitutionSettings()](#getSubstitutionSettings) | Einstellungen zum Schrift‑Substitutions‑Mechanismus. |
| [resetFontSources()](#resetFontSources) | Setzt die Schriftquellen auf die Systemstandardwerte zurück. |
| [saveSearchCache(OutputStream outputStream)](#saveSearchCache-java.io.OutputStream) |  |
| [setFontsFolder(String fontFolder, boolean recursive)](#setFontsFolder-java.lang.String-boolean) | Legt den Ordner fest, in dem Aspose.Words nach TrueType-Schriften sucht, wenn Dokumente gerendert oder Schriften eingebettet werden. |
| [setFontsFolders(String[] fontsFolders, boolean recursive)](#setFontsFolders-java.lang.String---boolean) | Legt die Ordner fest, in denen Aspose.Words nach TrueType-Schriften sucht, wenn Dokumente gerendert oder Schriften eingebettet werden. |
| [setFontsSources(FontSourceBase[] sources)](#setFontsSources-com.aspose.words.FontSourceBase) | Legt die Quellen fest, in denen Aspose.Words nach TrueType-Schriften sucht, wenn Dokumente gerendert oder Schriften eingebettet werden. |
| [setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)](#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream) |  |
### FontSettings() {#FontSettings}
```
public FontSettings()
```


Initialisiert eine neue Instanz dieser Klasse.

### getDefaultInstance() {#getDefaultInstance}
```
public static FontSettings getDefaultInstance()
```


Statische Standard‑Schriftarteinstellungen.

 **Remarks:** 

Diese Instanz wird standardmäßig in einem Dokument verwendet, sofern nicht [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings) angegeben ist.

 **Examples:** 

Zeigt, wie die Standard‑Schriftarteinstanz konfiguriert wird.

```

 // Configure the default font settings instance to use the "Courier New" font
 // as a backup substitute when we attempt to use an unknown font.
 FontSettings.getDefaultInstance().getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Courier New");

 Assert.assertTrue(FontSettings.getDefaultInstance().getSubstitutionSettings().getDefaultFontSubstitution().getEnabled());

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Non-existent font");
 builder.write("Hello world!");

 // This document does not have a FontSettings configuration. When we render the document,
 // the default FontSettings instance will resolve the missing font.
 // Aspose.Words will use "Courier New" to render text that uses the unknown font.
 Assert.assertNull(doc.getFontSettings());

 doc.save(getArtifactsDir() + "FontSettings.DefaultFontInstance.pdf");
 
```

Zeigt, wie das IWarningCallback‑Interface verwendet wird, um Warnungen bei Schriftart‑Ersetzungen zu überwachen.

```

 public void substitutionWarning() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.getFont().setName("Times New Roman");
     builder.writeln("Hello world!");

     FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
     doc.setWarningCallback(callback);

     // Store the current collection of font sources, which will be the default font source for every document
     // for which we do not specify a different font source.
     FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

     // For testing purposes, we will set Aspose.Words to look for fonts only in a folder that does not exist.
     FontSettings.getDefaultInstance().setFontsFolder("", false);

     // When rendering the document, there will be no place to find the "Times New Roman" font.
     // This will cause a font substitution warning, which our callback will detect.
     doc.save(getArtifactsDir() + "FontSettings.SubstitutionWarning.pdf");

     FontSettings.getDefaultInstance().setFontsSources(originalFontSources);

     Assert.assertTrue(callback.FontSubstitutionWarnings.get(0).getWarningType() == WarningType.FONT_SUBSTITUTION);
     Assert.assertTrue(callback.FontSubstitutionWarnings.get(0).getDescription()
             .equals("Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
 }

 private static class FontSubstitutionWarningCollector implements IWarningCallback {
     /// 
     /// Called every time a warning occurs during loading/saving.
     /// 
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
             FontSubstitutionWarnings.warning(info);
     }

     public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
 }
 
```

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getFallbackSettings() {#getFallbackSettings}
```
public FontFallbackSettings getFallbackSettings()
```


Einstellungen zum Schrift‑Fallback‑Mechanismus.

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

**Returns:**
[FontFallbackSettings](../../com.aspose.words/fontfallbacksettings/) - The corresponding [FontFallbackSettings](../../com.aspose.words/fontfallbacksettings/) value.
### getFontsSources() {#getFontsSources}
```
public FontSourceBase[] getFontsSources()
```


Gibt eine Kopie des Arrays zurück, das die Liste der Quellen enthält, in denen Aspose.Words nach TrueType-Schriften sucht.

 **Remarks:** 

Der zurückgegebene Wert ist eine Kopie der Daten, die Aspose.Words verwendet. Wenn Sie die Einträge im zurückgegebenen Array ändern, hat dies keine Auswirkung auf die Dokumentendarstellung. Um neue Schriftquellen anzugeben, verwenden Sie die Methode [setFontsSources(com.aspose.words.FontSourceBase[])](../../com.aspose.words/fontsettings/\#setFontsSources-com.aspose.words.FontSourceBase).

 **Examples:** 

Zeigt, wie eine Schriftquelle zu unseren bestehenden Schriftquellen hinzugefügt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Amethysta");
 builder.writeln("The quick brown fox jumps over the lazy dog.");
 builder.getFont().setName("Junction Light");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertEquals(1, originalFontSources.length);

 Assert.assertTrue(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));

 // The default font source is missing two of the fonts that we are using in our document.
 // When we save this document, Aspose.Words will apply fallback fonts to all text formatted with inaccessible fonts.
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Junction Light")));

 // Create a font source from a folder that contains fonts.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), true);

 // Apply a new array of font sources that contains the original font sources, as well as our custom fonts.
 FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
 FontSettings.getDefaultInstance().setFontsSources(updatedFontSources);

 // Verify that Aspose.Words has access to all required fonts before we render the document to PDF.
 updatedFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertTrue(IterableUtils.matchesAny(updatedFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));
 Assert.assertTrue(IterableUtils.matchesAny(updatedFontSources[1].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 Assert.assertTrue(IterableUtils.matchesAny(updatedFontSources[1].getAvailableFonts(), f -> f.getFullFontName().contains("Junction Light")));

 doc.save(getArtifactsDir() + "FontSettings.AddFontSource.pdf");

 // Restore the original font sources.
 FontSettings.getDefaultInstance().setFontsSources(originalFontSources);
 
```

**Returns:**
com.aspose.words.FontSourceBase[] - Eine Kopie der aktuellen Schriftquellen.
### getSubstitutionSettings() {#getSubstitutionSettings}
```
public FontSubstitutionSettings getSubstitutionSettings()
```


Einstellungen zum Schrift‑Substitutions‑Mechanismus.

 **Examples:** 

Zeigt, wie auf die System-Schriftartquelle eines Dokuments zugegriffen und Schriftart-Substitute festgelegt werden.

```

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());

 // By default, a blank document always contains a system font source.
 Assert.assertEquals(1, doc.getFontSettings().getFontsSources().length);

 SystemFontSource systemFontSource = (SystemFontSource) doc.getFontSettings().getFontsSources()[0];
 Assert.assertEquals(FontSourceType.SYSTEM_FONTS, systemFontSource.getType());
 Assert.assertEquals(0, systemFontSource.getPriority());

 if (SystemUtils.IS_OS_WINDOWS) {
     final String FONTS_PATH = "C:\\WINDOWS\\Fonts";
     Assert.assertEquals(FONTS_PATH.toLowerCase(), SystemFontSource.getSystemFontFolders()[0].toLowerCase());
 }

 for (String systemFontFolder : SystemFontSource.getSystemFontFolders()) {
     System.out.println(systemFontFolder);
 }

 // Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
 doc.getFontSettings().getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);
 doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().addSubstitutes("Kreon-Regular", "Calibri");

 Assert.assertEquals(1, IterableUtils.size(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")));
 Assert.assertTrue(IterableUtils.toString(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")).contains("Calibri"));

 // Alternatively, we could add a folder font source in which the corresponding folder contains the font.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false);
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{systemFontSource, folderFontSource});
 Assert.assertEquals(2, doc.getFontSettings().getFontsSources().length);

 // Resetting the font sources still leaves us with the system font source as well as our substitutes.
 doc.getFontSettings().resetFontSources();

 Assert.assertEquals(1, doc.getFontSettings().getFontsSources().length);
 Assert.assertEquals(FontSourceType.SYSTEM_FONTS, doc.getFontSettings().getFontsSources()[0].getType());
 Assert.assertEquals(1, IterableUtils.size(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")));
 Assert.assertTrue(doc.getFontSettings().getSubstitutionSettings().getFontNameSubstitution().getEnabled());
 
```

**Returns:**
[FontSubstitutionSettings](../../com.aspose.words/fontsubstitutionsettings/) - The corresponding [FontSubstitutionSettings](../../com.aspose.words/fontsubstitutionsettings/) value.
### resetFontSources() {#resetFontSources}
```
public void resetFontSources()
```


Setzt die Schriftquellen auf die Systemstandardwerte zurück.

 **Examples:** 

Zeigt, wie auf die System-Schriftartquelle eines Dokuments zugegriffen und Schriftart-Substitute festgelegt werden.

```

 Document doc = new Document();
 doc.setFontSettings(new FontSettings());

 // By default, a blank document always contains a system font source.
 Assert.assertEquals(1, doc.getFontSettings().getFontsSources().length);

 SystemFontSource systemFontSource = (SystemFontSource) doc.getFontSettings().getFontsSources()[0];
 Assert.assertEquals(FontSourceType.SYSTEM_FONTS, systemFontSource.getType());
 Assert.assertEquals(0, systemFontSource.getPriority());

 if (SystemUtils.IS_OS_WINDOWS) {
     final String FONTS_PATH = "C:\\WINDOWS\\Fonts";
     Assert.assertEquals(FONTS_PATH.toLowerCase(), SystemFontSource.getSystemFontFolders()[0].toLowerCase());
 }

 for (String systemFontFolder : SystemFontSource.getSystemFontFolders()) {
     System.out.println(systemFontFolder);
 }

 // Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
 doc.getFontSettings().getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);
 doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().addSubstitutes("Kreon-Regular", "Calibri");

 Assert.assertEquals(1, IterableUtils.size(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")));
 Assert.assertTrue(IterableUtils.toString(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")).contains("Calibri"));

 // Alternatively, we could add a folder font source in which the corresponding folder contains the font.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false);
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{systemFontSource, folderFontSource});
 Assert.assertEquals(2, doc.getFontSettings().getFontsSources().length);

 // Resetting the font sources still leaves us with the system font source as well as our substitutes.
 doc.getFontSettings().resetFontSources();

 Assert.assertEquals(1, doc.getFontSettings().getFontsSources().length);
 Assert.assertEquals(FontSourceType.SYSTEM_FONTS, doc.getFontSettings().getFontsSources()[0].getType());
 Assert.assertEquals(1, IterableUtils.size(doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().getSubstitutes("Kreon-Regular")));
 Assert.assertTrue(doc.getFontSettings().getSubstitutionSettings().getFontNameSubstitution().getEnabled());
 
```

### saveSearchCache(OutputStream outputStream) {#saveSearchCache-java.io.OutputStream}
```
public void saveSearchCache(OutputStream outputStream)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### setFontsFolder(String fontFolder, boolean recursive) {#setFontsFolder-java.lang.String-boolean}
```
public void setFontsFolder(String fontFolder, boolean recursive)
```


Legt den Ordner fest, in dem Aspose.Words nach TrueType-Schriften sucht, wenn Dokumente gerendert oder Schriften eingebettet werden. Dies ist eine Abkürzung zu [setFontsFolders(java.lang.String[], boolean)](../../com.aspose.words/fontsettings/\#setFontsFolders-java.lang.String----boolean), um nur ein Schriftverzeichnis festzulegen.

 **Examples:** 

Zeigt, wie ein Schriftquellen‑Verzeichnis festgelegt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arvo");
 builder.writeln("Hello world!");
 builder.getFont().setName("Amethysta");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 // Our font sources do not contain the font that we have used for text in this document.
 // If we use these font settings while rendering this document,
 // Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
 FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertEquals(1, originalFontSources.length);
 Assert.assertTrue(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));

 // The default font sources are missing the two fonts that we are using in this document.
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arvo")));
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));

 // Use the "SetFontsFolder" method to set a directory which will act as a new font source.
 // Pass "false" as the "recursive" argument to include fonts from all the font files that are in the directory
 // that we are passing in the first argument, but not include any fonts in any of that directory's subfolders.
 // Pass "true" as the "recursive" argument to include all font files in the directory that we are passing
 // in the first argument, as well as all the fonts in its subdirectories.
 FontSettings.getDefaultInstance().setFontsFolder(getFontsDir(), recursive);

 FontSourceBase[] newFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertEquals(1, newFontSources.length);
 Assert.assertFalse(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));
 Assert.assertTrue(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arvo")));

 // The "Amethysta" font is in a subfolder of the font directory.
 if (recursive) {
     Assert.assertEquals(30, newFontSources[0].getAvailableFonts().size());
     Assert.assertTrue(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 } else {
     Assert.assertEquals(18, newFontSources[0].getAvailableFonts().size());
     Assert.assertFalse(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 }

 doc.save(getArtifactsDir() + "FontSettings.SetFontsFolder.pdf");

 // Restore the original font sources.
 FontSettings.getDefaultInstance().setFontsSources(originalFontSources);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFolder | java.lang.String | Der Ordner, der TrueType-Schriften enthält. |
| recursive | boolean | True, um die angegebenen Ordner rekursiv nach Schriften zu durchsuchen. |

### setFontsFolders(String[] fontsFolders, boolean recursive) {#setFontsFolders-java.lang.String---boolean}
```
public void setFontsFolders(String[] fontsFolders, boolean recursive)
```


Legt die Ordner fest, in denen Aspose.Words nach TrueType-Schriften sucht, wenn Dokumente gerendert oder Schriften eingebettet werden.

 **Remarks:** 

Standardmäßig sucht Aspose.Words nach im System installierten Schriften.

Das Festlegen dieser Eigenschaft setzt den Cache aller zuvor geladenen Schriften zurück.

 **Examples:** 

Zeigt, wie mehrere Schriftquellen‑Verzeichnisse festgelegt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Amethysta");
 builder.writeln("The quick brown fox jumps over the lazy dog.");
 builder.getFont().setName("Junction Light");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 // Our font sources do not contain the font that we have used for text in this document.
 // If we use these font settings while rendering this document,
 // Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
 FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertEquals(1, originalFontSources.length);
 Assert.assertTrue(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));

 // The default font sources are missing the two fonts that we are using in this document.
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Junction Light")));

 // Use the "SetFontsFolders" method to create a font source from each font directory that we pass as the first argument.
 // Pass "false" as the "recursive" argument to include fonts from all the font files that are in the directories
 // that we are passing in the first argument, but not include any fonts from any of the directories' subfolders.
 // Pass "true" as the "recursive" argument to include all font files in the directories that we are passing
 // in the first argument, as well as all the fonts in their subdirectories.
 FontSettings.getDefaultInstance().setFontsFolders(new String[]{getFontsDir() + "/Amethysta", getFontsDir() + "/Junction"}, recursive);

 FontSourceBase[] newFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertEquals(2, newFontSources.length);
 Assert.assertFalse(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));
 Assert.assertEquals(1, newFontSources[0].getAvailableFonts().size());
 Assert.assertTrue(IterableUtils.matchesAny(newFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));

 // The "Junction" folder itself contains no font files, but has subfolders that do.
 if (recursive) {
     Assert.assertEquals(11, newFontSources[1].getAvailableFonts().size());
     Assert.assertTrue(IterableUtils.matchesAny(newFontSources[1].getAvailableFonts(), f -> f.getFullFontName().contains("Junction Light")));
 } else {
     Assert.assertEquals(0, newFontSources[1].getAvailableFonts().size());
 }

 doc.save(getArtifactsDir() + "FontSettings.SetFontsFolders.pdf");

 // Restore the original font sources.
 FontSettings.getDefaultInstance().setFontsSources(originalFontSources);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontsFolders | java.lang.String[] | Ein Array von Ordnern, die TrueType-Schriften enthalten. |
| recursive | boolean | True, um die angegebenen Ordner rekursiv nach Schriften zu durchsuchen. |

### setFontsSources(FontSourceBase[] sources) {#setFontsSources-com.aspose.words.FontSourceBase}
```
public void setFontsSources(FontSourceBase[] sources)
```


Legt die Quellen fest, in denen Aspose.Words nach TrueType-Schriften sucht, wenn Dokumente gerendert oder Schriften eingebettet werden.

 **Remarks:** 

Standardmäßig sucht Aspose.Words nach im System installierten Schriften.

Das Festlegen dieser Eigenschaft setzt den Cache aller zuvor geladenen Schriften zurück.

 **Examples:** 

Zeigt, wie eine Schriftquelle zu unseren bestehenden Schriftquellen hinzugefügt wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Amethysta");
 builder.writeln("The quick brown fox jumps over the lazy dog.");
 builder.getFont().setName("Junction Light");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertEquals(1, originalFontSources.length);

 Assert.assertTrue(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));

 // The default font source is missing two of the fonts that we are using in our document.
 // When we save this document, Aspose.Words will apply fallback fonts to all text formatted with inaccessible fonts.
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 Assert.assertFalse(IterableUtils.matchesAny(originalFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Junction Light")));

 // Create a font source from a folder that contains fonts.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), true);

 // Apply a new array of font sources that contains the original font sources, as well as our custom fonts.
 FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
 FontSettings.getDefaultInstance().setFontsSources(updatedFontSources);

 // Verify that Aspose.Words has access to all required fonts before we render the document to PDF.
 updatedFontSources = FontSettings.getDefaultInstance().getFontsSources();

 Assert.assertTrue(IterableUtils.matchesAny(updatedFontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));
 Assert.assertTrue(IterableUtils.matchesAny(updatedFontSources[1].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));
 Assert.assertTrue(IterableUtils.matchesAny(updatedFontSources[1].getAvailableFonts(), f -> f.getFullFontName().contains("Junction Light")));

 doc.save(getArtifactsDir() + "FontSettings.AddFontSource.pdf");

 // Restore the original font sources.
 FontSettings.getDefaultInstance().setFontsSources(originalFontSources);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase/) | Ein Array von Quellen, die TrueType-Schriften enthalten. |

### setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream) {#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream}
```
public void setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase/) |  |
| cacheInputStream | java.io.InputStream |  |

