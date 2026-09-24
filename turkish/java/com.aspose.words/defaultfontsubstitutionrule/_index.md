---
title: "DefaultFontSubstitutionRule"
linktitle: "DefaultFontSubstitutionRule"
second_title: "Aspose.Words Java için"
description: "Java'da varsayılan yazı tipi ikame kuralı."
type: docs
weight: 149
url: /tr/java/com.aspose.words/defaultfontsubstitutionrule/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule/)
```
public class DefaultFontSubstitutionRule extends FontSubstitutionRule
```

Varsayılan yazı tipi ikame kuralı.

Daha fazla bilgi için, [ Working with Fonts ][Working with Fonts] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bu kural, orijinal yazı tipi mevcut değilse ikame için kullanılacak tek varsayılan yazı tipi adını tanımlar.

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


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getDefaultFontName()](#getDefaultFontName) | Varsayılan yazı tipi adını alır. |
| [getEnabled()](#getEnabled) | Kuralın etkin olup olmadığını belirtir. |
| [setDefaultFontName(String value)](#setDefaultFontName-java.lang.String) | Varsayılan yazı tipi adını ayarlar. |
| [setEnabled(boolean value)](#setEnabled-boolean) | Kuralın etkin olup olmadığını belirtir. |
### getDefaultFontName() {#getDefaultFontName}
```
public String getDefaultFontName()
```


Varsayılan yazı tipi adını alır.

 **Remarks:** 

Varsayılan değer 'Times New Roman'dır.

 **Examples:** 

Varsayılan bir yazı tipinin nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Arvo");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 FontSourceBase[] fontSources = FontSettings.getDefaultInstance().getFontsSources();

 // The font sources that the document uses contain the font "Arial", but not "Arvo".
 Assert.assertEquals(1, fontSources.length);
 Assert.assertTrue(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));
 Assert.assertFalse(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arvo")));

 // Set the "DefaultFontName" property to "Courier New" to,
 // while rendering the document, apply that font in all cases when another font is not available.
 FontSettings.getDefaultInstance().getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Courier New");

 Assert.assertTrue(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Courier New")));

 // Aspose.Words will now use the default font in place of any missing fonts during any rendering calls.
 doc.save(getArtifactsDir() + "FontSettings.DefaultFontName.pdf");
 
```

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
java.lang.String - Varsayılan yazı tipi adı.
### getEnabled() {#getEnabled}
```
public boolean getEnabled()
```


Kuralın etkin olup olmadığını belirtir.

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
boolean - İlgili  boolean  değeri.
### setDefaultFontName(String value) {#setDefaultFontName-java.lang.String}
```
public void setDefaultFontName(String value)
```


Varsayılan yazı tipi adını ayarlar.

 **Remarks:** 

Varsayılan değer 'Times New Roman'dır.

 **Examples:** 

Varsayılan bir yazı tipinin nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Arvo");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 FontSourceBase[] fontSources = FontSettings.getDefaultInstance().getFontsSources();

 // The font sources that the document uses contain the font "Arial", but not "Arvo".
 Assert.assertEquals(1, fontSources.length);
 Assert.assertTrue(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));
 Assert.assertFalse(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arvo")));

 // Set the "DefaultFontName" property to "Courier New" to,
 // while rendering the document, apply that font in all cases when another font is not available.
 FontSettings.getDefaultInstance().getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Courier New");

 Assert.assertTrue(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Courier New")));

 // Aspose.Words will now use the default font in place of any missing fonts during any rendering calls.
 doc.save(getArtifactsDir() + "FontSettings.DefaultFontName.pdf");
 
```

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Varsayılan yazı tipi adı. |

### setEnabled(boolean value) {#setEnabled-boolean}
```
public void setEnabled(boolean value)
```


Kuralın etkin olup olmadığını belirtir.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

