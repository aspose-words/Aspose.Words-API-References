---
title: "FontSubstitutionSettings"
linktitle: "FontSubstitutionSettings"
second_title: "Aspose.Words لـ Java"
description: "يحدد إعدادات آلية استبدال الخط في Java."
type: docs
weight: 337
url: /ar/java/com.aspose.words/fontsubstitutionsettings/
---

**Inheritance:**
java.lang.Object
```
public class FontSubstitutionSettings
```

يحدد إعدادات آلية استبدال الخط.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

تتكون عملية استبدال الخط من عدة قواعد يتم فحصها واحدة تلو الأخرى بترتيب محدد. إذا لم تستطع القاعدة الأولى حل الخط، يتم فحص القاعدة الثانية وهكذا.

ترتيب القواعد كما يلي: 1. قاعدة استبدال اسم الخط (مفعلة افتراضيًا) 2. قاعدة استبدال إعدادات الخط (معطلة افتراضيًا) 3. قاعدة استبدال الجدول (مفعلة افتراضيًا) 4. قاعدة استبدال معلومات الخط (مفعلة افتراضيًا) 5. قاعدة الخط الافتراضي (مفعلة افتراضيًا)

لاحظ أن قاعدة استبدال معلومات الخط ستحل الخط دائمًا إذا كان [FontInfo](../../com.aspose.words/fontinfo/) متاحًا وستتجاوز قاعدة الخط الافتراضي. إذا كنت ترغب في استخدام قاعدة الخط الافتراضي، فيجب عليك تعطيل قاعدة استبدال معلومات الخط.

لاحظ أن قاعدة استبدال إعدادات الخط ستحل الخط في معظم الحالات وبالتالي تتجاوز جميع القواعد الأخرى.

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


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getDefaultFontSubstitution()](#getDefaultFontSubstitution) | الإعدادات المتعلقة بقاعدة استبدال الخط الافتراضي. |
| [getFontConfigSubstitution()](#getFontConfigSubstitution) | الإعدادات المتعلقة بقاعدة استبدال إعدادات الخط. |
| [getFontInfoSubstitution()](#getFontInfoSubstitution) | الإعدادات المتعلقة بقاعدة استبدال معلومات الخط. |
| [getFontNameSubstitution()](#getFontNameSubstitution) | الإعدادات المتعلقة بقاعدة استبدال اسم الخط. |
| [getTableSubstitution()](#getTableSubstitution) | الإعدادات المتعلقة بقاعدة استبدال الجدول. |
### getDefaultFontSubstitution() {#getDefaultFontSubstitution}
```
public DefaultFontSubstitutionRule getDefaultFontSubstitution()
```


الإعدادات المتعلقة بقاعدة استبدال الخط الافتراضي.

 **Examples:** 

يوضح كيفية تعيين قاعدة استبدال الخط الافتراضي.

```

 Document doc = new Document();
 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);

 // Get the default substitution rule within FontSettings.
 // This rule will substitute all missing fonts with "Times New Roman".
 DefaultFontSubstitutionRule defaultFontSubstitutionRule = fontSettings.getSubstitutionSettings().getDefaultFontSubstitution();
 Assert.assertTrue(defaultFontSubstitutionRule.getEnabled());
 Assert.assertEquals("Times New Roman", defaultFontSubstitutionRule.getDefaultFontName());

 // Set the default font substitute to "Courier New".
 defaultFontSubstitutionRule.setDefaultFontName("Courier New");

 // Using a document builder, add some text in a font that we do not have to see the substitution take place,
 // and then render the result in a PDF.
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Missing Font");
 builder.writeln("Line written in a missing font, which will be substituted with Courier New.");

 doc.save(getArtifactsDir() + "FontSettings.DefaultFontSubstitutionRule.pdf");
 
```

**Returns:**
[DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule/) - The corresponding [DefaultFontSubstitutionRule](../../com.aspose.words/defaultfontsubstitutionrule/) value.
### getFontConfigSubstitution() {#getFontConfigSubstitution}
```
public FontConfigSubstitutionRule getFontConfigSubstitution()
```


الإعدادات المتعلقة بقاعدة استبدال إعدادات الخط.

 **Examples:** 

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
[FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule/) - The corresponding [FontConfigSubstitutionRule](../../com.aspose.words/fontconfigsubstitutionrule/) value.
### getFontInfoSubstitution() {#getFontInfoSubstitution}
```
public FontInfoSubstitutionRule getFontInfoSubstitution()
```


الإعدادات المتعلقة بقاعدة استبدال معلومات الخط.

 **Examples:** 

يوضح كيفية تعيين الخاصية للعثور على أقرب تطابق للخط المفقود من مصادر الخطوط المتاحة.

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

**Returns:**
[FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule/) - The corresponding [FontInfoSubstitutionRule](../../com.aspose.words/fontinfosubstitutionrule/) value.
### getFontNameSubstitution() {#getFontNameSubstitution}
```
public FontNameSubstitutionRule getFontNameSubstitution()
```


الإعدادات المتعلقة بقاعدة استبدال اسم الخط.

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

**Returns:**
[FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule/) - The corresponding [FontNameSubstitutionRule](../../com.aspose.words/fontnamesubstitutionrule/) value.
### getTableSubstitution() {#getTableSubstitution}
```
public TableSubstitutionRule getTableSubstitution()
```


الإعدادات المتعلقة بقاعدة استبدال الجدول.

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

**Returns:**
[TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule/) - The corresponding [TableSubstitutionRule](../../com.aspose.words/tablesubstitutionrule/) value.
