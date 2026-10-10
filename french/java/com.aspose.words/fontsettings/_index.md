---
title: "FontSettings"
linktitle: "FontSettings"
second_title: "Aspose.Words pour Java"
description: "Spécifie les paramètres de police pour un document en Java."
type: docs
weight: 332
url: /fr/java/com.aspose.words/fontsettings/
---

**Inheritance:**
java.lang.Object
```
public class FontSettings
```

Spécifie les paramètres de police pour un document.

Pour en savoir plus, consultez l’article de documentation [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Aspose.Words utilise les paramètres de police pour résoudre les polices dans le document. Les polices sont résolues principalement lors de la construction de la mise en page du document ou du rendu vers des formats de page fixe. Mais lors du chargement de certains formats, Aspose.Words peut également devoir résoudre les polices. Par exemple, lors du chargement de documents HTML, Aspose.Words peut résoudre les polices pour effectuer le repli de police. Il est donc recommandé de définir les paramètres de police dans [LoadOptions](../../com.aspose.words/loadoptions/) lors du chargement du document. Ou au moins avant de construire la mise en page ou de rendre le document au format de page fixe.

Par défaut, tous les documents utilisent une seule instance statique de paramètres de police. Elle peut être accédée via la propriété [getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance).

Modifier les paramètres de police est sûr à tout moment depuis n'importe quel thread. Mais il est recommandé de ne pas modifier les paramètres de police pendant le traitement de certains documents qui utilisent ces paramètres. Cela peut entraîner le fait que la même police soit résolue différemment dans différentes parties du document.

 **Examples:** 

Montre comment définir un répertoire source de police.

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

Montre comment définir plusieurs répertoires sources de police.

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

Montre comment ajouter une source de police à nos sources de police existantes.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [FontSettings()](#FontSettings) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getDefaultInstance()](#getDefaultInstance) | Paramètres de police par défaut statiques. |
| [getFallbackSettings()](#getFallbackSettings) | Paramètres liés au mécanisme de repli de police. |
| [getFontsSources()](#getFontsSources) | Obtient une copie du tableau contenant la liste des sources où Aspose.Words recherche les polices TrueType. |
| [getSubstitutionSettings()](#getSubstitutionSettings) | Paramètres liés au mécanisme de substitution de police. |
| [resetFontSources()](#resetFontSources) | Réinitialise les sources de polices aux valeurs par défaut du système. |
| [saveSearchCache(OutputStream outputStream)](#saveSearchCache-java.io.OutputStream) |  |
| [setFontsFolder(String fontFolder, boolean recursive)](#setFontsFolder-java.lang.String-boolean) | Définit le dossier où Aspose.Words recherche les polices TrueType lors du rendu des documents ou de l'intégration des polices. |
| [setFontsFolders(String[] fontsFolders, boolean recursive)](#setFontsFolders-java.lang.String---boolean) | Définit les dossiers où Aspose.Words recherche les polices TrueType lors du rendu des documents ou de l'intégration des polices. |
| [setFontsSources(FontSourceBase[] sources)](#setFontsSources-com.aspose.words.FontSourceBase) | Définit les sources où Aspose.Words recherche les polices TrueType lors du rendu des documents ou de l'intégration des polices. |
| [setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)](#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream) |  |
### FontSettings() {#FontSettings}
```
public FontSettings()
```


Initialise une nouvelle instance de cette classe.

### getDefaultInstance() {#getDefaultInstance}
```
public static FontSettings getDefaultInstance()
```


Paramètres de police par défaut statiques.

 **Remarks:** 

Cette instance est utilisée par défaut dans un document sauf si [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings) est spécifié.

 **Examples:** 

Montre comment configurer l'instance des paramètres de police par défaut.

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

Montre comment utiliser l'interface IWarningCallback pour surveiller les avertissements de substitution de police.

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


Paramètres liés au mécanisme de repli de police.

 **Examples:** 

Montre comment répartir les polices de secours sur les plages de codes de caractères Unicode.

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


Obtient une copie du tableau contenant la liste des sources où Aspose.Words recherche les polices TrueType.

 **Remarks:** 

La valeur retournée est une copie des données utilisées par Aspose.Words. Si vous modifiez les entrées du tableau retourné, cela n'aura aucun effet sur le rendu du document. Pour spécifier de nouvelles sources de police, utilisez la méthode [setFontsSources(com.aspose.words.FontSourceBase[])](../../com.aspose.words/fontsettings/\#setFontsSources-com.aspose.words.FontSourceBase).

 **Examples:** 

Montre comment ajouter une source de police à nos sources de police existantes.

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
com.aspose.words.FontSourceBase[] - Une copie des sources de police actuelles.
### getSubstitutionSettings() {#getSubstitutionSettings}
```
public FontSubstitutionSettings getSubstitutionSettings()
```


Paramètres liés au mécanisme de substitution de police.

 **Examples:** 

Montre comment accéder à la source de polices système d'un document et définir des substituts de police.

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


Réinitialise les sources de polices aux valeurs par défaut du système.

 **Examples:** 

Montre comment accéder à la source de polices système d'un document et définir des substituts de police.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### setFontsFolder(String fontFolder, boolean recursive) {#setFontsFolder-java.lang.String-boolean}
```
public void setFontsFolder(String fontFolder, boolean recursive)
```


Définit le dossier où Aspose.Words recherche les polices TrueType lors du rendu des documents ou de l'intégration des polices. C'est un raccourci vers [setFontsFolders(java.lang.String[], boolean)](../../com.aspose.words/fontsettings/\#setFontsFolders-java.lang.String----boolean) pour définir un seul répertoire de police.

 **Examples:** 

Montre comment définir un répertoire source de police.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| fontFolder | java.lang.String | Le dossier qui contient les polices TrueType. |
| récursif | boolean | True pour analyser de façon récursive les dossiers spécifiés à la recherche de polices. |

### setFontsFolders(String[] fontsFolders, boolean recursive) {#setFontsFolders-java.lang.String---boolean}
```
public void setFontsFolders(String[] fontsFolders, boolean recursive)
```


Définit les dossiers où Aspose.Words recherche les polices TrueType lors du rendu des documents ou de l'intégration des polices.

 **Remarks:** 

Par défaut, Aspose.Words recherche les polices installées sur le système.

La définition de cette propriété réinitialise le cache de toutes les polices précédemment chargées.

 **Examples:** 

Montre comment définir plusieurs répertoires sources de police.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| fontsFolders | java.lang.String[] | Un tableau de dossiers contenant des polices TrueType. |
| récursif | boolean | True pour analyser de façon récursive les dossiers spécifiés à la recherche de polices. |

### setFontsSources(FontSourceBase[] sources) {#setFontsSources-com.aspose.words.FontSourceBase}
```
public void setFontsSources(FontSourceBase[] sources)
```


Définit les sources où Aspose.Words recherche les polices TrueType lors du rendu des documents ou de l'intégration des polices.

 **Remarks:** 

Par défaut, Aspose.Words recherche les polices installées sur le système.

La définition de cette propriété réinitialise le cache de toutes les polices précédemment chargées.

 **Examples:** 

Montre comment ajouter une source de police à nos sources de police existantes.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase/) | Un tableau de sources contenant des polices TrueType. |

### setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream) {#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream}
```
public void setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase/) |  |
| cacheInputStream | java.io.InputStream |  |

