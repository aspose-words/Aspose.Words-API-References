---
title: "TableSubstitutionRule"
linktitle: "TableSubstitutionRule"
second_title: "Aspose.Words لـ Java"
description: "قاعدة استبدال خطوط الجدول في Java."
type: docs
weight: 662
url: /ar/java/com.aspose.words/tablesubstitutionrule/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule/)
```
public class TableSubstitutionRule extends FontSubstitutionRule
```

قاعدة استبدال خط الجدول.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

تحدد هذه القاعدة قائمة أسماء الخطوط البديلة التي سيتم استخدامها إذا لم يتوفر الخط الأصلي. سيتم فحص البدائل لاسم الخط و[FontInfo.getAltName()](../../com.aspose.words/fontinfo/\#getAltName) / [FontInfo.setAltName(java.lang.String)](../../com.aspose.words/fontinfo/\#setAltName-java.lang.String) (إن وجدت).

 **Examples:** 

يوضح كيفية الوصول إلى جداول استبدال الخطوط لنظامي Windows وLinux.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [addSubstitutes(String originalFontName, String[] substituteFontNames)](#addSubstitutes-java.lang.String-java.lang.String...) | يضيف أسماء خطوط بديلة للخط الأصلي المحدد. |
| [getEnabled()](#getEnabled) | يحدد ما إذا كانت القاعدة مفعلة أم لا. |
| [getSubstitutes(String originalFontName)](#getSubstitutes-java.lang.String) | يرجع مصفوفة تحتوي على أسماء الخطوط البديلة للخط الأصلي المحدد. |
| [load(InputStream stream)](#load-java.io.InputStream) |  |
| [load(String fileName)](#load-java.lang.String) | يقوم بتحميل إعدادات استبدال الجدول من ملف XML. |
| [loadAndroidSettings()](#loadAndroidSettings) | يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Android. |
| [loadLinuxSettings()](#loadLinuxSettings) | يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Linux. |
| [loadWindowsSettings()](#loadWindowsSettings) | يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Windows. |
| [save(OutputStream outputStream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | يحفظ إعدادات استبدال الجدول الحالية إلى ملف. |
| [setEnabled(boolean value)](#setEnabled-boolean) | يحدد ما إذا كانت القاعدة مفعلة أم لا. |
| [setSubstitutes(String originalFontName, String[] substituteFontNames)](#setSubstitutes-java.lang.String-java.lang.String...) | يتجاوز أسماء الخطوط البديلة للخط الأصلي المحدد. |
### addSubstitutes(String originalFontName, String[] substituteFontNames) {#addSubstitutes-java.lang.String-java.lang.String...}
```
public void addSubstitutes(String originalFontName, String[] substituteFontNames)
```


يضيف أسماء خطوط بديلة للخط الأصلي المحدد.

 **Examples:** 

يوضح كيفية الوصول إلى مصدر الخطوط النظامي للمستند وتعيين بدائل الخط.

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

يوضح كيفية العمل مع جداول استبدال الخطوط المخصصة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| originalFontName | java.lang.String | اسم الخط الأصلي. |
| substituteFontNames | java.lang.String[] | قائمة بأسماء الخطوط البديلة. |

### getEnabled() {#getEnabled}
```
public boolean getEnabled()
```


يحدد ما إذا كانت القاعدة مفعلة أم لا.

 **Examples:** 

يوضح كيفية الوصول إلى مصدر الخطوط النظامي للمستند وتعيين بدائل الخط.

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

يوضح استبدال تكوين الخط المعتمد على نظام التشغيل.

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
boolean - القيمة المنطقية المقابلة.
### getSubstitutes(String originalFontName) {#getSubstitutes-java.lang.String}
```
public Iterable getSubstitutes(String originalFontName)
```


يرجع مصفوفة تحتوي على أسماء الخطوط البديلة للخط الأصلي المحدد.

 **Examples:** 

يوضح كيفية الوصول إلى مصدر الخطوط النظامي للمستند وتعيين بدائل الخط.

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

يوضح كيفية العمل مع جداول استبدال الخطوط المخصصة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| originalFontName | java.lang.String | اسم الخط الأصلي. |

**Returns:**
java.lang.Iterable - قائمة بأسماء الخطوط البديلة.
### load(InputStream stream) {#load-java.io.InputStream}
```
public void load(InputStream stream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### load(String fileName) {#load-java.lang.String}
```
public void load(String fileName)
```


يقوم بتحميل إعدادات استبدال الجدول من ملف XML.

 **Examples:** 

يوضح كيفية العمل مع جداول استبدال الخطوط المخصصة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | اسم ملف الإدخال. |

### loadAndroidSettings() {#loadAndroidSettings}
```
public void loadAndroidSettings()
```


يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Android.

### loadLinuxSettings() {#loadLinuxSettings}
```
public void loadLinuxSettings()
```


يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Linux.

 **Examples:** 

يوضح كيفية الوصول إلى جداول استبدال الخطوط لنظامي Windows وLinux.

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


يقوم بتحميل إعدادات استبدال الجدول المحددة مسبقًا لمنصة Windows.

 **Examples:** 

يوضح كيفية الوصول إلى جداول استبدال الخطوط لنظامي Windows وLinux.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


يحفظ إعدادات استبدال الجدول الحالية إلى ملف.

 **Examples:** 

يوضح كيفية الوصول إلى جداول استبدال الخطوط لنظامي Windows وLinux.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | اسم ملف الإخراج. |

### setEnabled(boolean value) {#setEnabled-boolean}
```
public void setEnabled(boolean value)
```


يحدد ما إذا كانت القاعدة مفعلة أم لا.

 **Examples:** 

يوضح كيفية الوصول إلى مصدر الخطوط النظامي للمستند وتعيين بدائل الخط.

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

يوضح استبدال تكوين الخط المعتمد على نظام التشغيل.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setSubstitutes(String originalFontName, String[] substituteFontNames) {#setSubstitutes-java.lang.String-java.lang.String...}
```
public void setSubstitutes(String originalFontName, String[] substituteFontNames)
```


يتجاوز أسماء الخطوط البديلة للخط الأصلي المحدد.

 **Examples:** 

يعرض كيفية تعيين قواعد استبدال الخطوط.

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

يوضح كيفية العمل مع جداول استبدال الخطوط المخصصة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| originalFontName | java.lang.String | اسم الخط الأصلي. |
| substituteFontNames | java.lang.String[] | قائمة بأسماء الخطوط البديلة. |

