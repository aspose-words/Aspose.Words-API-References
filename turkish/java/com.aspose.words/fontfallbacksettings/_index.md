---
title: "FontFallbackSettings"
linktitle: "FontFallbackSettings"
second_title: "Aspose.Words Java için"
description: "Java'da font geri dönüş mekanizması ayarlarını belirtir."
type: docs
weight: 323
url: /tr/java/com.aspose.words/fontfallbacksettings/
---

**Inheritance:**
java.lang.Object
```
public class FontFallbackSettings
```

Yazı tipi geri dönüş mekanizması ayarlarını belirtir.

Daha fazla bilgi için, [ Working with Fonts ][Working with Fonts] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Varsayılan olarak geri dönüş ayarları, Microsoft Word geri dönüşünü taklit eden önceden tanımlı ayarlarla başlatılır.

 **Examples:** 

Geri dönüş fontlarının Unicode karakter kod aralıkları arasında nasıl dağıtılacağını gösterir.

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


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [buildAutomatic()](#buildAutomatic) | Mevcut fontları tarayarak geri dönüş ayarlarını otomatik olarak oluşturur. |
| [load(InputStream stream)](#load-java.io.InputStream) |  |
| [load(String fileName)](#load-java.lang.String) | XML dosyasından font geri dönüş ayarlarını yükler. |
| [loadMsOfficeFallbackSettings()](#loadMsOfficeFallbackSettings) | Microsoft Word geri dönüşünü taklit eden ve Microsoft Office fontlarını kullanan önceden tanımlı geri dönüş ayarlarını yükler. |
| [loadNotoFallbackSettings()](#loadNotoFallbackSettings) | Google Noto fontlarını kullanan önceden tanımlı geri dönüş ayarlarını yükler. |
| [save(OutputStream outputStream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Mevcut geri dönüş ayarlarını dosyaya kaydeder. |
### buildAutomatic() {#buildAutomatic}
```
public void buildAutomatic()
```


Mevcut fontları tarayarak geri dönüş ayarlarını otomatik olarak oluşturur.

 **Remarks:** 

Bu yöntem, optimal olmayan geri dönüş ayarları üretebilir. Fontlar, gerçek glif varlığına göre değil, [ Unicode Character Range ][Unicode Character Range] alanlarıyla kontrol edilir. Ayrıca Unicode aralıkları ayrı ayrı kontrol edilir ve tek bir dil/skripte ilişkin birkaç aralık farklı geri dönüş fontları kullanabilir.

 **Examples:** 

Geri dönüş fontlarının Unicode karakter kod aralıkları arasında nasıl dağıtılacağını gösterir.

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


[Unicode Character Range]: https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur

### load(InputStream stream) {#load-java.io.InputStream}
```
public void load(InputStream stream)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### load(String fileName) {#load-java.lang.String}
```
public void load(String fileName)
```


XML dosyasından font geri dönüş ayarlarını yükler.

 **Examples:** 

Yerel dosya sistemindeki bir XML belgesine font geri dönüş ayarlarını yükleme ve kaydetme yöntemini gösterir.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Load an XML document that defines a set of font fallback settings.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getFallbackSettings().load(getMyDir() + "Font fallback rules.xml");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

 // Save our document's current font fallback settings as an XML document.
 doc.getFontSettings().getFallbackSettings().save(getArtifactsDir() + "FallbackSettings.xml");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Girdi dosya adı. |

### loadMsOfficeFallbackSettings() {#loadMsOfficeFallbackSettings}
```
public void loadMsOfficeFallbackSettings()
```


Microsoft Word geri dönüşünü taklit eden ve Microsoft Office fontlarını kullanan önceden tanımlı geri dönüş ayarlarını yükler.

 **Examples:** 

Önceden tanımlı geri dönüş font ayarlarını nasıl yükleyeceğinizi gösterir.

```

 Document doc = new Document();

 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);
 FontFallbackSettings fontFallbackSettings = fontSettings.getFallbackSettings();

 // Save the default fallback font scheme to an XML document.
 // For example, one of the elements has a value of "0C00-0C7F" for Range and a corresponding "Vani" value for FallbackFonts.
 // This means that if the font some text is using does not have symbols for the 0x0C00-0x0C7F Unicode block,
 // the fallback scheme will use symbols from the "Vani" font substitute.
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.Default.xml");

 // Below are two pre-defined font fallback schemes we can choose from.
 // 1 -  Use the default Microsoft Office scheme, which is the same one as the default:
 fontFallbackSettings.loadMsOfficeFallbackSettings();
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

 // 2 -  Use the scheme built from Google Noto fonts:
 fontFallbackSettings.loadNotoFallbackSettings();
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
 
```

### loadNotoFallbackSettings() {#loadNotoFallbackSettings}
```
public void loadNotoFallbackSettings()
```


Google Noto fontlarını kullanan önceden tanımlı geri dönüş ayarlarını yükler.

 **Examples:** 

Google Noto fontları için önceden tanımlı font geri dönüş ayarlarını nasıl ekleyeceğinizi gösterir.

```

 FontSettings fontSettings = new FontSettings();

 // These are free fonts licensed under the SIL Open Font License.
 // We can download the fonts here:
 // https://www.google.com/get/noto/#sans-lgc
 fontSettings.setFontsFolder(getFontsDir() + "Noto", false);

 // Note that the predefined settings only use Sans-style Noto fonts with regular weight.
 // Some of the Noto fonts use advanced typography features.
 // Fonts featuring advanced typography may not be rendered correctly as Aspose.Words currently do not support them.
 fontSettings.getFallbackSettings().loadNotoFallbackSettings();
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(false);
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Noto Sans");

 Document doc = new Document();
 doc.setFontSettings(fontSettings);
 
```

Önceden tanımlı geri dönüş font ayarlarını nasıl yükleyeceğinizi gösterir.

```

 Document doc = new Document();

 FontSettings fontSettings = new FontSettings();
 doc.setFontSettings(fontSettings);
 FontFallbackSettings fontFallbackSettings = fontSettings.getFallbackSettings();

 // Save the default fallback font scheme to an XML document.
 // For example, one of the elements has a value of "0C00-0C7F" for Range and a corresponding "Vani" value for FallbackFonts.
 // This means that if the font some text is using does not have symbols for the 0x0C00-0x0C7F Unicode block,
 // the fallback scheme will use symbols from the "Vani" font substitute.
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.Default.xml");

 // Below are two pre-defined font fallback schemes we can choose from.
 // 1 -  Use the default Microsoft Office scheme, which is the same one as the default:
 fontFallbackSettings.loadMsOfficeFallbackSettings();
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

 // 2 -  Use the scheme built from Google Noto fonts:
 fontFallbackSettings.loadNotoFallbackSettings();
 fontFallbackSettings.save(getArtifactsDir() + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
 
```

### save(OutputStream outputStream) {#save-java.io.OutputStream}
```
public void save(OutputStream outputStream)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Mevcut geri dönüş ayarlarını dosyaya kaydeder.

 **Examples:** 

Yerel dosya sistemindeki bir XML belgesine font geri dönüş ayarlarını yükleme ve kaydetme yöntemini gösterir.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Load an XML document that defines a set of font fallback settings.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getFallbackSettings().load(getMyDir() + "Font fallback rules.xml");

 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

 // Save our document's current font fallback settings as an XML document.
 doc.getFontSettings().getFallbackSettings().save(getArtifactsDir() + "FallbackSettings.xml");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Çıktı dosya adı. |

