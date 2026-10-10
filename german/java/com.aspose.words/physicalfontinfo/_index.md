---
title: "PhysicalFontInfo"
linktitle: "PhysicalFontInfo"
second_title: "Aspose.Words für Java"
description: "Gibt Informationen über physische Schriftarten an, die der Schrift-Engine von Aspose.Words in Java zur Verfügung stehen."
type: docs
weight: 548
url: /de/java/com.aspose.words/physicalfontinfo/
---

**Inheritance:**
java.lang.Object
```
public class PhysicalFontInfo
```

Gibt Informationen über physische Schriftarten an, die dem Aspose.Words‑Schrift‑Engine zur Verfügung stehen.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Fonts ][Working with Fonts].

 **Examples:** 

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getEmbeddingLicensingRights()](#getEmbeddingLicensingRights) | Einbetten von Lizenzrechten für die Schriftart. |
| [getFilePath()](#getFilePath) | Pfad zur Schriftdatei, falls vorhanden. |
| [getFontFamilyName()](#getFontFamilyName) | Familienname der Schriftart. |
| [getFullFontName()](#getFullFontName) | Vollständiger Name der Schriftart. |
| [getVersion()](#getVersion) | Versionszeichenfolge der Schriftart. |
### getEmbeddingLicensingRights() {#getEmbeddingLicensingRights}
```
public FontEmbeddingLicensingRights getEmbeddingLicensingRights()
```


Einbetten von Lizenzrechten für die Schriftart.

 **Examples:** 

Zeigt, wie Lizenzrechtsinformationen für eingebettete Schriftarten (PhysicalFontInfo) abgerufen werden.

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


Pfad zur Schriftdatei, falls vorhanden.

 **Examples:** 

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getFontFamilyName() {#getFontFamilyName}
```
public String getFontFamilyName()
```


Familienname der Schriftart.

 **Examples:** 

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getFullFontName() {#getFullFontName}
```
public String getFullFontName()
```


Vollständiger Name der Schriftart.

 **Examples:** 

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getVersion() {#getVersion}
```
public String getVersion()
```


Versionszeichenfolge der Schriftart.

 **Examples:** 

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
