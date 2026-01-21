---
title: TableSubstitutionRule
linktitle: TableSubstitutionRule
second_title: Aspose.Words for Java
description: Table font substitution rule in Java.
type: docs
weight: 659
url: /java/com.aspose.words/tablesubstitutionrule/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule/)
```
public class TableSubstitutionRule extends FontSubstitutionRule
```

Table font substitution rule.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.

 **Remarks:** 

This rule defines the list of substitute font names to be used if the original font is not available. Substitutes will be checked for the font name and the [FontInfo.getAltName()](../../com.aspose.words/fontinfo/\#getAltName) / [FontInfo.setAltName(java.lang.String)](../../com.aspose.words/fontinfo/\#setAltName-java.lang.String) (if any).

 **Examples:** 

Shows how to access font substitution tables for Windows and Linux.

```

 Document doc = new Document();
 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);

 // Create a new table substitution rule and load the default Microsoft Windows font substitution table.
 TableSubstitutionRule tableSubstitutionRule = fontSettings.getSubstitutionSettings().getTableSubstitution();
 tableSubstitutionRule.loadWindowsSettings();

 // In Windows, the default substitute for the "Times New Roman CE" font is "Times New Roman".
 Assert.assertEquals(new String[]{"Times New Roman"},
         IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman CE")).toArray());

 // We can save the table in the form of an XML document.
 tableSubstitutionRule.save(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Windows.xml");

 // Linux has its own substitution table.
 // There are multiple substitute fonts for "Times New Roman CE".
 // If the first substitute, "FreeSerif" is also unavailable,
 // this rule will cycle through the others in the array until it finds an available one.
 tableSubstitutionRule.loadLinuxSettings();
 Assert.assertEquals(new String[]{"FreeSerif", "Liberation Serif", "DejaVu Serif"},
         IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman CE")).toArray());

 // Save the Linux substitution table in the form of an XML document using a stream.
 try (FileOutputStream fileStream = new FileOutputStream(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Linux.xml")) {
     tableSubstitutionRule.save(fileStream);
 }
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Methods

| Method | Description |
| --- | --- |
| [addSubstitutes(String originalFontName, String[] substituteFontNames)](#addSubstitutes-java.lang.String-java.lang.String...) | Adds substitute font names for given original font name. |
| [getEnabled()](#getEnabled) | Specifies whether the rule is enabled or not. |
| [getSubstitutes(String originalFontName)](#getSubstitutes-java.lang.String) | Returns array containing substitute font names for the specified original font name. |
| [load(InputStream stream)](#load-java.io.InputStream) |  |
| [load(String fileName)](#load-java.lang.String) | Loads table substitution settings from XML file. |
| [loadAndroidSettings()](#loadAndroidSettings) | Loads predefined table substitution settings for Android platform. |
| [loadLinuxSettings()](#loadLinuxSettings) | Loads predefined table substitution settings for Linux platform. |
| [loadWindowsSettings()](#loadWindowsSettings) | Loads predefined table substitution settings for Windows platform. |
| [save(OutputStream outputStream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Saves the current table substitution settings to file. |
| [setEnabled(boolean value)](#setEnabled-boolean) | Specifies whether the rule is enabled or not. |
| [setSubstitutes(String originalFontName, String[] substituteFontNames)](#setSubstitutes-java.lang.String-java.lang.String...) | Override substitute font names for given original font name. |
### addSubstitutes(String originalFontName, String[] substituteFontNames) {#addSubstitutes-java.lang.String-java.lang.String...}
```
public void addSubstitutes(String originalFontName, String[] substituteFontNames)
```


Adds substitute font names for given original font name.

 **Examples:** 

Shows how to access a document's system font source and set font substitutes.

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

Shows how to work with custom font substitution tables.

```

 Document doc = new Document();
 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);

 // Create a new table substitution rule and load the default Windows font substitution table.
 TableSubstitutionRule tableSubstitutionRule = fontSettings.getSubstitutionSettings().getTableSubstitution();

 // If we select fonts exclusively from our folder, we will need a custom substitution table.
 // We will no longer have access to the Microsoft Windows fonts,
 // such as "Arial" or "Times New Roman" since they do not exist in our new font folder.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false);
 fontSettings.setFontsSources(new FontSourceBase[]{folderFontSource});

 // Below are two ways of loading a substitution table from a file in the local file system.
 // 1 -  From a stream:
 try (FileInputStream fileStream = new FileInputStream(getMyDir() + "Font substitution rules.xml")) {
     tableSubstitutionRule.load(fileStream);
 }

 // 2 -  Directly from a file:
 tableSubstitutionRule.load(getMyDir() + "Font substitution rules.xml");

 // Since we no longer have access to "Arial", our font table will first try substitute it with "Nonexistent Font".
 // We do not have this font so that it will move onto the next substitute, "Kreon", found in the "MyFonts" folder.
 Assert.assertEquals(new String[]{"Missing Font", "Kreon"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Arial")).toArray());

 // We can expand this table programmatically. We will add an entry that substitutes "Times New Roman" with "Arvo"
 Assert.assertNull(tableSubstitutionRule.getSubstitutes("Times New Roman"));
 tableSubstitutionRule.addSubstitutes("Times New Roman", "Arvo");
 Assert.assertEquals(new String[]{"Arvo"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // We can add a secondary fallback substitute for an existing font entry with AddSubstitutes().
 // In case "Arvo" is unavailable, our table will look for "M+ 2m" as a second substitute option.
 tableSubstitutionRule.addSubstitutes("Times New Roman", "M+ 2m");
 Assert.assertEquals(new String[]{"M+ 2m", "Arvo"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // SetSubstitutes() can set a new list of substitute fonts for a font.
 tableSubstitutionRule.setSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
 Assert.assertEquals(new String[]{"Squarish Sans CT", "M+ 2m"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // Writing text in fonts that we do not have access to will invoke our substitution rules.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Arial");
 builder.writeln("Text written in Arial, to be substituted by Kreon.");

 builder.getFont().setName("Times New Roman");
 builder.writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

 doc.save(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Custom.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | java.lang.String | Original font name. |
| substituteFontNames | java.lang.String[] | List of alternative font names. |

### getEnabled() {#getEnabled}
```
public boolean getEnabled()
```


Specifies whether the rule is enabled or not.

 **Examples:** 

Shows operating system-dependent font config substitution.

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

Shows how to access a document's system font source and set font substitutes.

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
boolean - The corresponding  boolean  value.
### getSubstitutes(String originalFontName) {#getSubstitutes-java.lang.String}
```
public Iterable getSubstitutes(String originalFontName)
```


Returns array containing substitute font names for the specified original font name.

 **Examples:** 

Shows how to access a document's system font source and set font substitutes.

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

Shows how to work with custom font substitution tables.

```

 Document doc = new Document();
 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);

 // Create a new table substitution rule and load the default Windows font substitution table.
 TableSubstitutionRule tableSubstitutionRule = fontSettings.getSubstitutionSettings().getTableSubstitution();

 // If we select fonts exclusively from our folder, we will need a custom substitution table.
 // We will no longer have access to the Microsoft Windows fonts,
 // such as "Arial" or "Times New Roman" since they do not exist in our new font folder.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false);
 fontSettings.setFontsSources(new FontSourceBase[]{folderFontSource});

 // Below are two ways of loading a substitution table from a file in the local file system.
 // 1 -  From a stream:
 try (FileInputStream fileStream = new FileInputStream(getMyDir() + "Font substitution rules.xml")) {
     tableSubstitutionRule.load(fileStream);
 }

 // 2 -  Directly from a file:
 tableSubstitutionRule.load(getMyDir() + "Font substitution rules.xml");

 // Since we no longer have access to "Arial", our font table will first try substitute it with "Nonexistent Font".
 // We do not have this font so that it will move onto the next substitute, "Kreon", found in the "MyFonts" folder.
 Assert.assertEquals(new String[]{"Missing Font", "Kreon"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Arial")).toArray());

 // We can expand this table programmatically. We will add an entry that substitutes "Times New Roman" with "Arvo"
 Assert.assertNull(tableSubstitutionRule.getSubstitutes("Times New Roman"));
 tableSubstitutionRule.addSubstitutes("Times New Roman", "Arvo");
 Assert.assertEquals(new String[]{"Arvo"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // We can add a secondary fallback substitute for an existing font entry with AddSubstitutes().
 // In case "Arvo" is unavailable, our table will look for "M+ 2m" as a second substitute option.
 tableSubstitutionRule.addSubstitutes("Times New Roman", "M+ 2m");
 Assert.assertEquals(new String[]{"M+ 2m", "Arvo"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // SetSubstitutes() can set a new list of substitute fonts for a font.
 tableSubstitutionRule.setSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
 Assert.assertEquals(new String[]{"Squarish Sans CT", "M+ 2m"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // Writing text in fonts that we do not have access to will invoke our substitution rules.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Arial");
 builder.writeln("Text written in Arial, to be substituted by Kreon.");

 builder.getFont().setName("Times New Roman");
 builder.writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

 doc.save(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Custom.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | java.lang.String | Original font name. |

**Returns:**
java.lang.Iterable - List of alternative font names.
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


Loads table substitution settings from XML file.

 **Examples:** 

Shows how to work with custom font substitution tables.

```

 Document doc = new Document();
 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);

 // Create a new table substitution rule and load the default Windows font substitution table.
 TableSubstitutionRule tableSubstitutionRule = fontSettings.getSubstitutionSettings().getTableSubstitution();

 // If we select fonts exclusively from our folder, we will need a custom substitution table.
 // We will no longer have access to the Microsoft Windows fonts,
 // such as "Arial" or "Times New Roman" since they do not exist in our new font folder.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false);
 fontSettings.setFontsSources(new FontSourceBase[]{folderFontSource});

 // Below are two ways of loading a substitution table from a file in the local file system.
 // 1 -  From a stream:
 try (FileInputStream fileStream = new FileInputStream(getMyDir() + "Font substitution rules.xml")) {
     tableSubstitutionRule.load(fileStream);
 }

 // 2 -  Directly from a file:
 tableSubstitutionRule.load(getMyDir() + "Font substitution rules.xml");

 // Since we no longer have access to "Arial", our font table will first try substitute it with "Nonexistent Font".
 // We do not have this font so that it will move onto the next substitute, "Kreon", found in the "MyFonts" folder.
 Assert.assertEquals(new String[]{"Missing Font", "Kreon"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Arial")).toArray());

 // We can expand this table programmatically. We will add an entry that substitutes "Times New Roman" with "Arvo"
 Assert.assertNull(tableSubstitutionRule.getSubstitutes("Times New Roman"));
 tableSubstitutionRule.addSubstitutes("Times New Roman", "Arvo");
 Assert.assertEquals(new String[]{"Arvo"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // We can add a secondary fallback substitute for an existing font entry with AddSubstitutes().
 // In case "Arvo" is unavailable, our table will look for "M+ 2m" as a second substitute option.
 tableSubstitutionRule.addSubstitutes("Times New Roman", "M+ 2m");
 Assert.assertEquals(new String[]{"M+ 2m", "Arvo"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // SetSubstitutes() can set a new list of substitute fonts for a font.
 tableSubstitutionRule.setSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
 Assert.assertEquals(new String[]{"Squarish Sans CT", "M+ 2m"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // Writing text in fonts that we do not have access to will invoke our substitution rules.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Arial");
 builder.writeln("Text written in Arial, to be substituted by Kreon.");

 builder.getFont().setName("Times New Roman");
 builder.writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

 doc.save(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Custom.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Input file name. |

### loadAndroidSettings() {#loadAndroidSettings}
```
public void loadAndroidSettings()
```


Loads predefined table substitution settings for Android platform.

### loadLinuxSettings() {#loadLinuxSettings}
```
public void loadLinuxSettings()
```


Loads predefined table substitution settings for Linux platform.

 **Examples:** 

Shows how to access font substitution tables for Windows and Linux.

```

 Document doc = new Document();
 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);

 // Create a new table substitution rule and load the default Microsoft Windows font substitution table.
 TableSubstitutionRule tableSubstitutionRule = fontSettings.getSubstitutionSettings().getTableSubstitution();
 tableSubstitutionRule.loadWindowsSettings();

 // In Windows, the default substitute for the "Times New Roman CE" font is "Times New Roman".
 Assert.assertEquals(new String[]{"Times New Roman"},
         IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman CE")).toArray());

 // We can save the table in the form of an XML document.
 tableSubstitutionRule.save(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Windows.xml");

 // Linux has its own substitution table.
 // There are multiple substitute fonts for "Times New Roman CE".
 // If the first substitute, "FreeSerif" is also unavailable,
 // this rule will cycle through the others in the array until it finds an available one.
 tableSubstitutionRule.loadLinuxSettings();
 Assert.assertEquals(new String[]{"FreeSerif", "Liberation Serif", "DejaVu Serif"},
         IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman CE")).toArray());

 // Save the Linux substitution table in the form of an XML document using a stream.
 try (FileOutputStream fileStream = new FileOutputStream(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Linux.xml")) {
     tableSubstitutionRule.save(fileStream);
 }
 
```

### loadWindowsSettings() {#loadWindowsSettings}
```
public void loadWindowsSettings()
```


Loads predefined table substitution settings for Windows platform.

 **Examples:** 

Shows how to access font substitution tables for Windows and Linux.

```

 Document doc = new Document();
 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);

 // Create a new table substitution rule and load the default Microsoft Windows font substitution table.
 TableSubstitutionRule tableSubstitutionRule = fontSettings.getSubstitutionSettings().getTableSubstitution();
 tableSubstitutionRule.loadWindowsSettings();

 // In Windows, the default substitute for the "Times New Roman CE" font is "Times New Roman".
 Assert.assertEquals(new String[]{"Times New Roman"},
         IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman CE")).toArray());

 // We can save the table in the form of an XML document.
 tableSubstitutionRule.save(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Windows.xml");

 // Linux has its own substitution table.
 // There are multiple substitute fonts for "Times New Roman CE".
 // If the first substitute, "FreeSerif" is also unavailable,
 // this rule will cycle through the others in the array until it finds an available one.
 tableSubstitutionRule.loadLinuxSettings();
 Assert.assertEquals(new String[]{"FreeSerif", "Liberation Serif", "DejaVu Serif"},
         IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman CE")).toArray());

 // Save the Linux substitution table in the form of an XML document using a stream.
 try (FileOutputStream fileStream = new FileOutputStream(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Linux.xml")) {
     tableSubstitutionRule.save(fileStream);
 }
 
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


Saves the current table substitution settings to file.

 **Examples:** 

Shows how to access font substitution tables for Windows and Linux.

```

 Document doc = new Document();
 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);

 // Create a new table substitution rule and load the default Microsoft Windows font substitution table.
 TableSubstitutionRule tableSubstitutionRule = fontSettings.getSubstitutionSettings().getTableSubstitution();
 tableSubstitutionRule.loadWindowsSettings();

 // In Windows, the default substitute for the "Times New Roman CE" font is "Times New Roman".
 Assert.assertEquals(new String[]{"Times New Roman"},
         IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman CE")).toArray());

 // We can save the table in the form of an XML document.
 tableSubstitutionRule.save(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Windows.xml");

 // Linux has its own substitution table.
 // There are multiple substitute fonts for "Times New Roman CE".
 // If the first substitute, "FreeSerif" is also unavailable,
 // this rule will cycle through the others in the array until it finds an available one.
 tableSubstitutionRule.loadLinuxSettings();
 Assert.assertEquals(new String[]{"FreeSerif", "Liberation Serif", "DejaVu Serif"},
         IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman CE")).toArray());

 // Save the Linux substitution table in the form of an XML document using a stream.
 try (FileOutputStream fileStream = new FileOutputStream(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Linux.xml")) {
     tableSubstitutionRule.save(fileStream);
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Output file name. |

### setEnabled(boolean value) {#setEnabled-boolean}
```
public void setEnabled(boolean value)
```


Specifies whether the rule is enabled or not.

 **Examples:** 

Shows operating system-dependent font config substitution.

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

Shows how to access a document's system font source and set font substitutes.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSubstitutes(String originalFontName, String[] substituteFontNames) {#setSubstitutes-java.lang.String-java.lang.String...}
```
public void setSubstitutes(String originalFontName, String[] substituteFontNames)
```


Override substitute font names for given original font name.

 **Examples:** 

Shows how set font substitution rules.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Amethysta");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 FontSourceBase[] fontSources = FontSettings.getDefaultInstance().getFontsSources();

 // The default font sources contain the first font that the document uses.
 Assert.assertEquals(1, fontSources.length);
 Assert.assertTrue(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));

 // The second font, "Amethysta", is unavailable.
 Assert.assertFalse(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));

 // We can configure a font substitution table which determines
 // which fonts Aspose.Words will use as substitutes for unavailable fonts.
 // Set two substitution fonts for "Amethysta": "Arvo", and "Courier New".
 // If the first substitute is unavailable, Aspose.Words attempts to use the second substitute, and so on.
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().setSubstitutes(
         "Amethysta", "Arvo", "Courier New");

 // "Amethysta" is unavailable, and the substitution rule states that the first font to use as a substitute is "Arvo".
 Assert.assertFalse(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arvo")));

 // "Arvo" is also unavailable, but "Courier New" is.
 Assert.assertTrue(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Courier New")));

 // The output document will display the text that uses the "Amethysta" font formatted with "Courier New".
 doc.save(getArtifactsDir() + "FontSettings.TableSubstitution.pdf");
 
```

Shows how to work with custom font substitution tables.

```

 Document doc = new Document();
 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);

 // Create a new table substitution rule and load the default Windows font substitution table.
 TableSubstitutionRule tableSubstitutionRule = fontSettings.getSubstitutionSettings().getTableSubstitution();

 // If we select fonts exclusively from our folder, we will need a custom substitution table.
 // We will no longer have access to the Microsoft Windows fonts,
 // such as "Arial" or "Times New Roman" since they do not exist in our new font folder.
 FolderFontSource folderFontSource = new FolderFontSource(getFontsDir(), false);
 fontSettings.setFontsSources(new FontSourceBase[]{folderFontSource});

 // Below are two ways of loading a substitution table from a file in the local file system.
 // 1 -  From a stream:
 try (FileInputStream fileStream = new FileInputStream(getMyDir() + "Font substitution rules.xml")) {
     tableSubstitutionRule.load(fileStream);
 }

 // 2 -  Directly from a file:
 tableSubstitutionRule.load(getMyDir() + "Font substitution rules.xml");

 // Since we no longer have access to "Arial", our font table will first try substitute it with "Nonexistent Font".
 // We do not have this font so that it will move onto the next substitute, "Kreon", found in the "MyFonts" folder.
 Assert.assertEquals(new String[]{"Missing Font", "Kreon"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Arial")).toArray());

 // We can expand this table programmatically. We will add an entry that substitutes "Times New Roman" with "Arvo"
 Assert.assertNull(tableSubstitutionRule.getSubstitutes("Times New Roman"));
 tableSubstitutionRule.addSubstitutes("Times New Roman", "Arvo");
 Assert.assertEquals(new String[]{"Arvo"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // We can add a secondary fallback substitute for an existing font entry with AddSubstitutes().
 // In case "Arvo" is unavailable, our table will look for "M+ 2m" as a second substitute option.
 tableSubstitutionRule.addSubstitutes("Times New Roman", "M+ 2m");
 Assert.assertEquals(new String[]{"M+ 2m", "Arvo"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // SetSubstitutes() can set a new list of substitute fonts for a font.
 tableSubstitutionRule.setSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
 Assert.assertEquals(new String[]{"Squarish Sans CT", "M+ 2m"}, IterableUtils.toList(tableSubstitutionRule.getSubstitutes("Times New Roman")).toArray());

 // Writing text in fonts that we do not have access to will invoke our substitution rules.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setName("Arial");
 builder.writeln("Text written in Arial, to be substituted by Kreon.");

 builder.getFont().setName("Times New Roman");
 builder.writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

 doc.save(getArtifactsDir() + "FontSettings.TableSubstitutionRule.Custom.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| originalFontName | java.lang.String | Original font name. |
| substituteFontNames | java.lang.String[] | List of alternative font names. |

