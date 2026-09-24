---
title: "FontSubstitutionSettings"
linktitle: "FontSubstitutionSettings"
second_title: "Aspose.Words Java için"
description: "Java'da yazı tipi ikame mekanizması ayarlarını belirtir."
type: docs
weight: 337
url: /tr/java/com.aspose.words/fontsubstitutionsettings/
---

**Inheritance:**
java.lang.Object
```
public class FontSubstitutionSettings
```

Yazı tipi ikame mekanizması ayarlarını belirtir.

Daha fazla bilgi için, [ Working with Fonts ][Working with Fonts] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Yazı tipi ikame süreci, belirli bir sırada tek tek kontrol edilen birkaç kuraldan oluşur. İlk kural yazı tipini çözemiyorsa ikinci kural kontrol edilir ve bu şekilde devam eder.

Kuralların sırası şu şekildedir: 1. Yazı tipi adı ikame kuralı (varsayılan olarak etkin) 2. Yazı tipi yapılandırma ikame kuralı (varsayılan olarak devre dışı) 3. Tablo ikame kuralı (varsayılan olarak etkin) 4. Yazı tipi bilgisi ikame kuralı (varsayılan olarak etkin) 5. Varsayılan yazı tipi kuralı (varsayılan olarak etkin)

Not: Yazı tipi bilgisi ikame kuralı, [FontInfo](../../com.aspose.words/fontinfo/) mevcutsa her zaman yazı tipini çözer ve varsayılan yazı tipi kuralını geçersiz kılar. Varsayılan yazı tipi kuralını kullanmak istiyorsanız, yazı tipi bilgisi ikame kuralını devre dışı bırakmalısınız.

Not: Yazı tipi yapılandırma ikame kuralı, çoğu durumda yazı tipini çözer ve bu nedenle diğer tüm kuralları geçersiz kılar.

 **Examples:** 

Bir belgenin sistem yazı tipi kaynağına nasıl erişileceğini ve yazı tipi ikamelerinin nasıl ayarlanacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getDefaultFontSubstitution()](#getDefaultFontSubstitution) | Varsayılan yazı tipi ikame kuralıyla ilgili ayarlar. |
| [getFontConfigSubstitution()](#getFontConfigSubstitution) | Yazı tipi yapılandırma ikame kuralıyla ilgili ayarlar. |
| [getFontInfoSubstitution()](#getFontInfoSubstitution) | Yazı tipi bilgisi ikame kuralıyla ilgili ayarlar. |
| [getFontNameSubstitution()](#getFontNameSubstitution) | Yazı tipi adı ikame kuralıyla ilgili ayarlar. |
| [getTableSubstitution()](#getTableSubstitution) | Tablo ikame kuralıyla ilgili ayarlar. |
### getDefaultFontSubstitution() {#getDefaultFontSubstitution}
```
public DefaultFontSubstitutionRule getDefaultFontSubstitution()
```


Varsayılan yazı tipi ikame kuralıyla ilgili ayarlar.

 **Examples:** 

Varsayılan yazı tipi ikame kuralının nasıl ayarlanacağını gösterir.

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


Yazı tipi yapılandırma ikame kuralıyla ilgili ayarlar.

 **Examples:** 

İşletim sistemi bağımlı yazı tipi yapılandırma ikamesini gösterir.

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


Yazı tipi bilgisi ikame kuralıyla ilgili ayarlar.

 **Examples:** 

Mevcut yazı tipi kaynaklarından eksik bir yazı tipi için en yakın eşleşmeyi bulmak üzere özelliğin nasıl ayarlanacağını gösterir.

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


Yazı tipi adı ikame kuralıyla ilgili ayarlar.

 **Examples:** 

Bir belgenin sistem yazı tipi kaynağına nasıl erişileceğini ve yazı tipi ikamelerinin nasıl ayarlanacağını gösterir.

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


Tablo ikame kuralıyla ilgili ayarlar.

 **Examples:** 

Özel yazı tipi ikame tabloları ile nasıl çalışılacağını gösterir.

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
