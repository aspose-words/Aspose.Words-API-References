---
title: "FontInfoSubstitutionRule"
linktitle: "FontInfoSubstitutionRule"
second_title: "Aspose.Words für Java"
description: "Schriftinfo-Substitutionsregel in Java."
type: docs
weight: 328
url: /de/java/com.aspose.words/fontinfosubstitutionrule/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule/)
```
public class FontInfoSubstitutionRule extends FontSubstitutionRule
```

Schriftinfo‑Ersetzungsregel.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Gemäß dieser Regel bewertet Aspose.Words alle zugehörigen Felder in [FontInfo](../../com.aspose.words/fontinfo/) (Panose, Sig usw.) für die fehlende Schriftart und findet die am besten passende unter den verfügbaren Schriftquellen. Wenn [FontInfo](../../com.aspose.words/fontinfo/) für die fehlende Schriftart nicht verfügbar ist, wird nichts unternommen.

 **Examples:** 

Zeigt, wie die Eigenschaft zum Finden der besten Übereinstimmung für eine fehlende Schriftart aus den verfügbaren Schriftquellen festgelegt wird.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getEnabled()](#getEnabled) | Gibt an, ob die Regel aktiviert ist oder nicht. |
| [setEnabled(boolean value)](#setEnabled-boolean) | Gibt an, ob die Regel aktiviert ist oder nicht. |
### getEnabled() {#getEnabled}
```
public boolean getEnabled()
```


Gibt an, ob die Regel aktiviert ist oder nicht.

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

Zeigt betriebssystemabhängige Schriftart-Konfigurationssubstitution.

```

 FontSettings fontSettings = new FontSettings();
 FontConfigSubstitutionRule fontConfigSubstitution = fontSettings.getSubstitutionSettings().getFontConfigSubstitution();

 // The FontConfigSubstitutionRule object works differently on Windows/non-Windows platforms.
 // On Windows, it is unavailable.
 if (SystemUtils.IS_OS_WINDOWS) {
     Assert.assertFalse(fontConfigSubstitution.getEnabled());
     Assert.assertFalse(fontConfigSubstitution.isFontConfigAvailable());
 }

 // On Linux/Mac, we will have access to it, and will be able to perform operations.
 if (SystemUtils.IS_OS_LINUX) {
     Assert.assertTrue(fontConfigSubstitution.getEnabled());
     Assert.assertTrue(fontConfigSubstitution.isFontConfigAvailable());

     fontConfigSubstitution.resetCache();
 }
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### setEnabled(boolean value) {#setEnabled-boolean}
```
public void setEnabled(boolean value)
```


Gibt an, ob die Regel aktiviert ist oder nicht.

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

Zeigt betriebssystemabhängige Schriftart-Konfigurationssubstitution.

```

 FontSettings fontSettings = new FontSettings();
 FontConfigSubstitutionRule fontConfigSubstitution = fontSettings.getSubstitutionSettings().getFontConfigSubstitution();

 // The FontConfigSubstitutionRule object works differently on Windows/non-Windows platforms.
 // On Windows, it is unavailable.
 if (SystemUtils.IS_OS_WINDOWS) {
     Assert.assertFalse(fontConfigSubstitution.getEnabled());
     Assert.assertFalse(fontConfigSubstitution.isFontConfigAvailable());
 }

 // On Linux/Mac, we will have access to it, and will be able to perform operations.
 if (SystemUtils.IS_OS_LINUX) {
     Assert.assertTrue(fontConfigSubstitution.getEnabled());
     Assert.assertTrue(fontConfigSubstitution.isFontConfigAvailable());

     fontConfigSubstitution.resetCache();
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

