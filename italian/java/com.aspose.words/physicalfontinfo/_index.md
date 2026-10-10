---
title: "PhysicalFontInfo"
linktitle: "PhysicalFontInfo"
second_title: "Aspose.Words per Java"
description: "Specifica le informazioni sul font fisico disponibili per il motore dei font di Aspose.Words in Java."
type: docs
weight: 548
url: /it/java/com.aspose.words/physicalfontinfo/
---

**Inheritance:**
java.lang.Object
```
public class PhysicalFontInfo
```

Specifica le informazioni sul font fisico disponibile per il motore di font di Aspose.Words.

Per saperne di più, visita l'articolo di documentazione [ Working with Fonts ][Working with Fonts].

 **Examples:** 

Mostra come elencare i caratteri disponibili.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getEmbeddingLicensingRights()](#getEmbeddingLicensingRights) | Diritti di licenza per l'incorporamento del font. |
| [getFilePath()](#getFilePath) | Percorso al file del font, se presente. |
| [getFontFamilyName()](#getFontFamilyName) | Nome della famiglia del font. |
| [getFullFontName()](#getFullFontName) | Nome completo del font. |
| [getVersion()](#getVersion) | Stringa della versione del font. |
### getEmbeddingLicensingRights() {#getEmbeddingLicensingRights}
```
public FontEmbeddingLicensingRights getEmbeddingLicensingRights()
```


Diritti di licenza per l'incorporamento del font.

 **Examples:** 

Mostra come ottenere le informazioni sui diritti di licenza per i caratteri incorporati (PhysicalFontInfo).

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


Percorso al file del font, se presente.

 **Examples:** 

Mostra come elencare i caratteri disponibili.

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
java.lang.String - Il valore java.lang.String corrispondente.
### getFontFamilyName() {#getFontFamilyName}
```
public String getFontFamilyName()
```


Nome della famiglia del font.

 **Examples:** 

Mostra come elencare i caratteri disponibili.

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
java.lang.String - Il valore java.lang.String corrispondente.
### getFullFontName() {#getFullFontName}
```
public String getFullFontName()
```


Nome completo del font.

 **Examples:** 

Mostra come elencare i caratteri disponibili.

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
java.lang.String - Il valore java.lang.String corrispondente.
### getVersion() {#getVersion}
```
public String getVersion()
```


Stringa della versione del font.

 **Examples:** 

Mostra come elencare i caratteri disponibili.

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
java.lang.String - Il valore java.lang.String corrispondente.
