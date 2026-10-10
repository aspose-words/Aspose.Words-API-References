---
title: "PhysicalFontInfo"
linktitle: "PhysicalFontInfo"
second_title: "Aspose.Words Java için"
description: "Aspose.Words font motorunun Java'da kullanabileceği fiziksel font hakkında bilgi belirtir."
type: docs
weight: 548
url: /tr/java/com.aspose.words/physicalfontinfo/
---

**Inheritance:**
java.lang.Object
```
public class PhysicalFontInfo
```

Aspose.Words yazı tipi motorunda mevcut fiziksel yazı tipi hakkında bilgi belirtir.

Daha fazla bilgi için, [ Working with Fonts ][Working with Fonts] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Kullanılabilir yazı tiplerini listelemenin nasıl yapılacağını gösterir.

```

 // Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
 FontSourceBase[] folderFontSource = {new FolderFontSource(getFontsDir(), true)};

 for (PhysicalFontInfo fontInfo : folderFontSource[0].getAvailableFonts()) {
     System.out.println(MessageFormat.format("FontFamilyName : {0}", fontInfo.getFontFamilyName()));
     System.out.println(MessageFormat.format("FullFontName  : {0}", fontInfo.getFullFontName()));
     System.out.println(MessageFormat.format("Version  : {0}", fontInfo.getVersion()));
     System.out.println(MessageFormat.format("FilePath : {0}\n", fontInfo.getFilePath()));
 }
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getEmbeddingLicensingRights()](#getEmbeddingLicensingRights) | Font için gömme lisans hakları. |
| [getFilePath()](#getFilePath) | Varsa font dosyasının yolu. |
| [getFontFamilyName()](#getFontFamilyName) | Fontun aile adı. |
| [getFullFontName()](#getFullFontName) | Fontun tam adı. |
| [getVersion()](#getVersion) | Fontun sürüm dizesi. |
### getEmbeddingLicensingRights() {#getEmbeddingLicensingRights}
```
public FontEmbeddingLicensingRights getEmbeddingLicensingRights()
```


Font için gömme lisans hakları.

 **Examples:** 

Gömülü yazı tipleri için lisans hakları bilgilerini (PhysicalFontInfo) nasıl alacağınızı gösterir.

```

 FontSettings settings = FontSettings.getDefaultInstance();
 FontSourceBase source = settings.getFontsSources()[0];

 // Get the list of available fonts.
 ArrayList fontInfos = source.getAvailableFonts();
 for (PhysicalFontInfo fontInfo : fontInfos)
 {
     if (fontInfo.getEmbeddingLicensingRights() != null)
     {
         System.out.println(fontInfo.getEmbeddingLicensingRights().getEmbeddingUsagePermissions());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getBitmapEmbeddingOnly());
         System.out.println(fontInfo.getEmbeddingLicensingRights().getNoSubsetting());
     }
 }
 
```

**Returns:**
[FontEmbeddingLicensingRights](../../com.aspose.words/fontembeddinglicensingrights/) - The corresponding [FontEmbeddingLicensingRights](../../com.aspose.words/fontembeddinglicensingrights/) value.
### getFilePath() {#getFilePath}
```
public String getFilePath()
```


Varsa font dosyasının yolu.

 **Examples:** 

Kullanılabilir yazı tiplerini listelemenin nasıl yapılacağını gösterir.

```

 // Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
 FontSourceBase[] folderFontSource = {new FolderFontSource(getFontsDir(), true)};

 for (PhysicalFontInfo fontInfo : folderFontSource[0].getAvailableFonts()) {
     System.out.println(MessageFormat.format("FontFamilyName : {0}", fontInfo.getFontFamilyName()));
     System.out.println(MessageFormat.format("FullFontName  : {0}", fontInfo.getFullFontName()));
     System.out.println(MessageFormat.format("Version  : {0}", fontInfo.getVersion()));
     System.out.println(MessageFormat.format("FilePath : {0}\n", fontInfo.getFilePath()));
 }
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getFontFamilyName() {#getFontFamilyName}
```
public String getFontFamilyName()
```


Fontun aile adı.

 **Examples:** 

Kullanılabilir yazı tiplerini listelemenin nasıl yapılacağını gösterir.

```

 // Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
 FontSourceBase[] folderFontSource = {new FolderFontSource(getFontsDir(), true)};

 for (PhysicalFontInfo fontInfo : folderFontSource[0].getAvailableFonts()) {
     System.out.println(MessageFormat.format("FontFamilyName : {0}", fontInfo.getFontFamilyName()));
     System.out.println(MessageFormat.format("FullFontName  : {0}", fontInfo.getFullFontName()));
     System.out.println(MessageFormat.format("Version  : {0}", fontInfo.getVersion()));
     System.out.println(MessageFormat.format("FilePath : {0}\n", fontInfo.getFilePath()));
 }
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getFullFontName() {#getFullFontName}
```
public String getFullFontName()
```


Fontun tam adı.

 **Examples:** 

Kullanılabilir yazı tiplerini listelemenin nasıl yapılacağını gösterir.

```

 // Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
 FontSourceBase[] folderFontSource = {new FolderFontSource(getFontsDir(), true)};

 for (PhysicalFontInfo fontInfo : folderFontSource[0].getAvailableFonts()) {
     System.out.println(MessageFormat.format("FontFamilyName : {0}", fontInfo.getFontFamilyName()));
     System.out.println(MessageFormat.format("FullFontName  : {0}", fontInfo.getFullFontName()));
     System.out.println(MessageFormat.format("Version  : {0}", fontInfo.getVersion()));
     System.out.println(MessageFormat.format("FilePath : {0}\n", fontInfo.getFilePath()));
 }
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getVersion() {#getVersion}
```
public String getVersion()
```


Fontun sürüm dizesi.

 **Examples:** 

Kullanılabilir yazı tiplerini listelemenin nasıl yapılacağını gösterir.

```

 // Configure Aspose.Words to source fonts from a custom folder, and then print every available font.
 FontSourceBase[] folderFontSource = {new FolderFontSource(getFontsDir(), true)};

 for (PhysicalFontInfo fontInfo : folderFontSource[0].getAvailableFonts()) {
     System.out.println(MessageFormat.format("FontFamilyName : {0}", fontInfo.getFontFamilyName()));
     System.out.println(MessageFormat.format("FullFontName  : {0}", fontInfo.getFullFontName()));
     System.out.println(MessageFormat.format("Version  : {0}", fontInfo.getVersion()));
     System.out.println(MessageFormat.format("FilePath : {0}\n", fontInfo.getFilePath()));
 }
 
```

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
