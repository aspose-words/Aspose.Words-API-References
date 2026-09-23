---
title: "FontSettings"
linktitle: "FontSettings"
second_title: "Aspose.Words per Java"
description: "Specifica le impostazioni dei caratteri per un documento in Java."
type: docs
weight: 332
url: /it/java/com.aspose.words/fontsettings/
---

**Inheritance:**
java.lang.Object
```
public class FontSettings
```

Specifica le impostazioni del font per un documento.

Per saperne di più, visita l'articolo di documentazione [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Aspose.Words utilizza le impostazioni dei caratteri per risolvere i font nel documento. I font vengono risolti principalmente durante la costruzione del layout del documento o il rendering in formati a pagina fissa. Tuttavia, durante il caricamento di alcuni formati, Aspose.Words può anche dover risolvere i font. Per esempio, durante il caricamento di documenti HTML Aspose.Words può risolvere i font per eseguire il fallback dei caratteri. Perciò è consigliato impostare le impostazioni dei caratteri in [LoadOptions](../../com.aspose.words/loadoptions/) quando si carica il documento. O almeno prima di costruire il layout o renderizzare il documento nel formato a pagina fissa.

Per impostazione predefinita tutti i documenti utilizzano un'unica istanza statica delle impostazioni dei caratteri. È possibile accedervi tramite la proprietà [getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance).

Modificare le impostazioni dei caratteri è sicuro in qualsiasi momento da qualsiasi thread. Tuttavia è consigliato non modificare le impostazioni dei caratteri durante l'elaborazione di alcuni documenti che le utilizzano. Questo può portare al fatto che lo stesso font venga risolto in modo diverso in parti diverse del documento.

 **Examples:** 

Mostra come impostare una directory di origine dei font.

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

Mostra come impostare più directory di origine dei font.

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

Mostra come aggiungere una fonte di font alle nostre font source esistenti.

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
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [FontSettings()](#FontSettings) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getDefaultInstance()](#getDefaultInstance) | Impostazioni predefinite dei font statiche. |
| [getFallbackSettings()](#getFallbackSettings) | Impostazioni relative al meccanismo di fallback dei font. |
| [getFontsSources()](#getFontsSources) | Ottiene una copia dell'array che contiene l'elenco delle font source dove Aspose.Words cerca i font TrueType. |
| [getSubstitutionSettings()](#getSubstitutionSettings) | Impostazioni relative al meccanismo di sostituzione dei font. |
| [resetFontSources()](#resetFontSources) | Ripristina le font source alle impostazioni predefinite di sistema. |
| [saveSearchCache(OutputStream outputStream)](#saveSearchCache-java.io.OutputStream) |  |
| [setFontsFolder(String fontFolder, boolean recursive)](#setFontsFolder-java.lang.String-boolean) | Imposta la cartella in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font. |
| [setFontsFolders(String[] fontsFolders, boolean recursive)](#setFontsFolders-java.lang.String---boolean) | Imposta le cartelle in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font. |
| [setFontsSources(FontSourceBase[] sources)](#setFontsSources-com.aspose.words.FontSourceBase) | Imposta le font source in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font. |
| [setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)](#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream) |  |
### FontSettings() {#FontSettings}
```
public FontSettings()
```


Inizializza una nuova istanza di questa classe.

### getDefaultInstance() {#getDefaultInstance}
```
public static FontSettings getDefaultInstance()
```


Impostazioni predefinite dei font statiche.

 **Remarks:** 

Questa istanza è utilizzata per impostazione predefinita in un documento a meno che non vengano specificati [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings).

 **Examples:** 

Mostra come configurare l'istanza predefinita delle impostazioni dei font.

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

Mostra come utilizzare l'interfaccia IWarningCallback per monitorare gli avvisi di sostituzione dei caratteri.

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


Impostazioni relative al meccanismo di fallback dei font.

 **Examples:** 

Mostra come distribuire i font di fallback attraverso gli intervalli di codici dei caratteri Unicode.

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


Ottiene una copia dell'array che contiene l'elenco delle font source dove Aspose.Words cerca i font TrueType.

 **Remarks:** 

Il valore restituito è una copia dei dati utilizzati da Aspose.Words. Se si modificano le voci nell'array restituito, non avranno alcun effetto sul rendering del documento. Per specificare nuove font source utilizzare il metodo [setFontsSources(com.aspose.words.FontSourceBase[])](../../com.aspose.words/fontsettings/\#setFontsSources-com.aspose.words.FontSourceBase).

 **Examples:** 

Mostra come aggiungere una fonte di font alle nostre font source esistenti.

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
com.aspose.words.FontSourceBase[] - Una copia delle font source attuali.
### getSubstitutionSettings() {#getSubstitutionSettings}
```
public FontSubstitutionSettings getSubstitutionSettings()
```


Impostazioni relative al meccanismo di sostituzione dei font.

 **Examples:** 

Mostra come accedere alla fonte dei caratteri di sistema di un documento e impostare i sostituti dei caratteri.

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


Ripristina le font source alle impostazioni predefinite di sistema.

 **Examples:** 

Mostra come accedere alla fonte dei caratteri di sistema di un documento e impostare i sostituti dei caratteri.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### setFontsFolder(String fontFolder, boolean recursive) {#setFontsFolder-java.lang.String-boolean}
```
public void setFontsFolder(String fontFolder, boolean recursive)
```


Imposta la cartella in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font. Questo è un collegamento rapido a [setFontsFolders(java.lang.String[], boolean)](../../com.aspose.words/fontsettings/\#setFontsFolders-java.lang.String----boolean) per impostare una sola directory di font.

 **Examples:** 

Mostra come impostare una directory di origine dei font.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontFolder | java.lang.String | La cartella che contiene i font TrueType. |
| ricorsivo | boolean | True per eseguire la scansione ricorsiva delle cartelle specificate alla ricerca di caratteri. |

### setFontsFolders(String[] fontsFolders, boolean recursive) {#setFontsFolders-java.lang.String---boolean}
```
public void setFontsFolders(String[] fontsFolders, boolean recursive)
```


Imposta le cartelle in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font.

 **Remarks:** 

Per impostazione predefinita, Aspose.Words cerca i caratteri installati nel sistema.

Impostare questa proprietà reimposta la cache di tutti i caratteri precedentemente caricati.

 **Examples:** 

Mostra come impostare più directory di origine dei font.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontsFolders | java.lang.String[] | Un array di cartelle che contengono caratteri TrueType. |
| ricorsivo | boolean | True per eseguire la scansione ricorsiva delle cartelle specificate alla ricerca di caratteri. |

### setFontsSources(FontSourceBase[] sources) {#setFontsSources-com.aspose.words.FontSourceBase}
```
public void setFontsSources(FontSourceBase[] sources)
```


Imposta le font source in cui Aspose.Words cerca i font TrueType durante il rendering dei documenti o l'incorporamento dei font.

 **Remarks:** 

Per impostazione predefinita, Aspose.Words cerca i caratteri installati nel sistema.

Impostare questa proprietà reimposta la cache di tutti i caratteri precedentemente caricati.

 **Examples:** 

Mostra come aggiungere una fonte di font alle nostre font source esistenti.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase/) | Un array di origini che contengono caratteri TrueType. |

### setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream) {#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream}
```
public void setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase/) |  |
| cacheInputStream | java.io.InputStream |  |

