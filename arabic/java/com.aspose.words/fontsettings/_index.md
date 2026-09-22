---
title: "FontSettings"
linktitle: "FontSettings"
second_title: "Aspose.Words لـ Java"
description: "يحدد إعدادات الخط لمستند في Java."
type: docs
weight: 332
url: /ar/java/com.aspose.words/fontsettings/
---

**Inheritance:**
java.lang.Object
```
public class FontSettings
```

يحدد إعدادات الخط لمستند.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

يستخدم Aspose.Words إعدادات الخط لتحديد الخطوط في المستند. يتم تحديد الخطوط في الغالب عند بناء تخطيط المستند أو عند العرض بصيغ الصفحات الثابتة. ولكن عند تحميل بعض الصيغ، قد يحتاج Aspose.Words أيضًا إلى تحديد الخطوط. على سبيل المثال، عند تحميل مستندات HTML قد يقوم Aspose.Words بتحديد الخطوط لتنفيذ fallback للخط. لذلك يُنصح بتعيين إعدادات الخط في [LoadOptions](../../com.aspose.words/loadoptions/) عند تحميل المستند. أو على الأقل قبل بناء التخطيط أو عرض المستند بصيغة الصفحة الثابتة.

بشكل افتراضي، تستخدم جميع المستندات نسخة واحدة ثابتة من إعدادات الخط. يمكن الوصول إليها عبر الخاصية [getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance).

تغيير إعدادات الخط آمن في أي وقت ومن أي خيط. ولكن يُنصح بعدم تغيير إعدادات الخط أثناء معالجة بعض المستندات التي تستخدم هذه الإعدادات. قد يؤدي ذلك إلى حل الخط نفسه بشكل مختلف في أجزاء مختلفة من المستند.

 **Examples:** 

يوضح كيفية تعيين دليل مصدر الخط.

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

يوضح كيفية تعيين عدة أدلة لمصادر الخط.

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

يوضح كيفية إضافة مصدر خط إلى مصادر الخط الحالية لدينا.

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [FontSettings()](#FontSettings) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getDefaultInstance()](#getDefaultInstance) | إعدادات الخط الافتراضية الثابتة. |
| [getFallbackSettings()](#getFallbackSettings) | الإعدادات المتعلقة بآلية fallback للخط. |
| [getFontsSources()](#getFontsSources) | يحصل على نسخة من المصفوفة التي تحتوي على قائمة المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType. |
| [getSubstitutionSettings()](#getSubstitutionSettings) | الإعدادات المتعلقة بآلية استبدال الخط. |
| [resetFontSources()](#resetFontSources) | يعيد تعيين مصادر الخط إلى الإعداد الافتراضي للنظام. |
| [saveSearchCache(OutputStream outputStream)](#saveSearchCache-java.io.OutputStream) |  |
| [setFontsFolder(String fontFolder, boolean recursive)](#setFontsFolder-java.lang.String-boolean) | يضبط المجلد الذي يبحث فيه Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. |
| [setFontsFolders(String[] fontsFolders, boolean recursive)](#setFontsFolders-java.lang.String---boolean) | يضبط المجلدات التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. |
| [setFontsSources(FontSourceBase[] sources)](#setFontsSources-com.aspose.words.FontSourceBase) | يضبط المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. |
| [setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)](#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream) |  |
### FontSettings() {#FontSettings}
```
public FontSettings()
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

### getDefaultInstance() {#getDefaultInstance}
```
public static FontSettings getDefaultInstance()
```


إعدادات الخط الافتراضية الثابتة.

 **Remarks:** 

يُستخدم هذا الكائن بشكل افتراضي في المستند ما لم يتم تحديد [Document.getFontSettings()](../../com.aspose.words/document/\#getFontSettings) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document/\#setFontSettings-com.aspose.words.FontSettings).

 **Examples:** 

يوضح كيفية تكوين نسخة إعدادات الخط الافتراضية.

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

يوضح كيفية استخدام واجهة IWarningCallback لمراقبة تحذيرات استبدال الخط.

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


الإعدادات المتعلقة بآلية fallback للخط.

 **Examples:** 

يعرض كيفية توزيع خطوط الاستبدال عبر نطاقات رموز الأحرف Unicode.

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


يحصل على نسخة من المصفوفة التي تحتوي على قائمة المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType.

 **Remarks:** 

القيمة المرجعة هي نسخة من البيانات التي يستخدمها Aspose.Words. إذا قمت بتغيير العناصر في المصفوفة المرجعة، فلن يؤثر ذلك على عرض المستند. لتحديد مصادر خطوط جديدة استخدم الطريقة [setFontsSources(com.aspose.words.FontSourceBase[])](../../com.aspose.words/fontsettings/\#setFontsSources-com.aspose.words.FontSourceBase).

 **Examples:** 

يوضح كيفية إضافة مصدر خط إلى مصادر الخط الحالية لدينا.

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
com.aspose.words.FontSourceBase[] - نسخة من مصادر الخط الحالية.
### getSubstitutionSettings() {#getSubstitutionSettings}
```
public FontSubstitutionSettings getSubstitutionSettings()
```


الإعدادات المتعلقة بآلية استبدال الخط.

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
[FontSubstitutionSettings](../../com.aspose.words/fontsubstitutionsettings/) - The corresponding [FontSubstitutionSettings](../../com.aspose.words/fontsubstitutionsettings/) value.
### resetFontSources() {#resetFontSources}
```
public void resetFontSources()
```


يعيد تعيين مصادر الخط إلى الإعداد الافتراضي للنظام.

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

### saveSearchCache(OutputStream outputStream) {#saveSearchCache-java.io.OutputStream}
```
public void saveSearchCache(OutputStream outputStream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### setFontsFolder(String fontFolder, boolean recursive) {#setFontsFolder-java.lang.String-boolean}
```
public void setFontsFolder(String fontFolder, boolean recursive)
```


يضبط المجلد الذي يبحث فيه Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط. هذا اختصار إلى [setFontsFolders(java.lang.String[], boolean)](../../com.aspose.words/fontsettings/\#setFontsFolders-java.lang.String----boolean) لتعيين دليل خط واحد فقط.

 **Examples:** 

يوضح كيفية تعيين دليل مصدر الخط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontFolder | java.lang.String | المجلد الذي يحتوي على خطوط TrueType. |
| متكرر | boolean | صحيح لمسح المجلدات المحددة للخطوط بشكل متكرر. |

### setFontsFolders(String[] fontsFolders, boolean recursive) {#setFontsFolders-java.lang.String---boolean}
```
public void setFontsFolders(String[] fontsFolders, boolean recursive)
```


يضبط المجلدات التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط.

 **Remarks:** 

افتراضيًا، يبحث Aspose.Words عن الخطوط المثبتة على النظام.

تعيين هذه الخاصية يعيد ضبط ذاكرة التخزين المؤقت لجميع الخطوط التي تم تحميلها مسبقًا.

 **Examples:** 

يوضح كيفية تعيين عدة أدلة لمصادر الخط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontsFolders | java.lang.String[] | مصفوفة من المجلدات التي تحتوي على خطوط TrueType. |
| متكرر | boolean | صحيح لمسح المجلدات المحددة للخطوط بشكل متكرر. |

### setFontsSources(FontSourceBase[] sources) {#setFontsSources-com.aspose.words.FontSourceBase}
```
public void setFontsSources(FontSourceBase[] sources)
```


يضبط المصادر التي يبحث فيها Aspose.Words عن خطوط TrueType عند عرض المستندات أو تضمين الخطوط.

 **Remarks:** 

افتراضيًا، يبحث Aspose.Words عن الخطوط المثبتة على النظام.

تعيين هذه الخاصية يعيد ضبط ذاكرة التخزين المؤقت لجميع الخطوط التي تم تحميلها مسبقًا.

 **Examples:** 

يوضح كيفية إضافة مصدر خط إلى مصادر الخط الحالية لدينا.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase/) | مصفوفة من المصادر التي تحتوي على خطوط TrueType. |

### setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream) {#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream}
```
public void setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase/) |  |
| cacheInputStream | java.io.InputStream |  |

