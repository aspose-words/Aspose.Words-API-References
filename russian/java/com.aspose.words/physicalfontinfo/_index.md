---
title: "PhysicalFontInfo"
linktitle: "PhysicalFontInfo"
second_title: "Aspose.Words для Java"
description: "Указывает информацию о физическом шрифте, доступном движку шрифтов Aspose.Words в Java."
type: docs
weight: 548
url: /ru/java/com.aspose.words/physicalfontinfo/
---

**Inheritance:**
java.lang.Object
```
public class PhysicalFontInfo
```

Указывает информацию о физическом шрифте, доступном движку шрифтов Aspose.Words.

Чтобы узнать больше, посетите статью документации [ Working with Fonts ][Working with Fonts].

 **Examples:** 

Показывает, как вывести список доступных шрифтов.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getEmbeddingLicensingRights()](#getEmbeddingLicensingRights) | Права лицензии на встраивание шрифта. |
| [getFilePath()](#getFilePath) | Путь к файлу шрифта, если он есть. |
| [getFontFamilyName()](#getFontFamilyName) | Семейное имя шрифта. |
| [getFullFontName()](#getFullFontName) | Полное имя шрифта. |
| [getVersion()](#getVersion) | Строка версии шрифта. |
### getEmbeddingLicensingRights() {#getEmbeddingLicensingRights}
```
public FontEmbeddingLicensingRights getEmbeddingLicensingRights()
```


Права лицензии на встраивание шрифта.

 **Examples:** 

Показывает, как получить информацию о правах лицензии для встроенных шрифтов (PhysicalFontInfo).

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


Путь к файлу шрифта, если он есть.

 **Examples:** 

Показывает, как вывести список доступных шрифтов.

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
java.lang.String - Соответствующее значение java.lang.String.
### getFontFamilyName() {#getFontFamilyName}
```
public String getFontFamilyName()
```


Семейное имя шрифта.

 **Examples:** 

Показывает, как вывести список доступных шрифтов.

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
java.lang.String - Соответствующее значение java.lang.String.
### getFullFontName() {#getFullFontName}
```
public String getFullFontName()
```


Полное имя шрифта.

 **Examples:** 

Показывает, как вывести список доступных шрифтов.

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
java.lang.String - Соответствующее значение java.lang.String.
### getVersion() {#getVersion}
```
public String getVersion()
```


Строка версии шрифта.

 **Examples:** 

Показывает, как вывести список доступных шрифтов.

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
java.lang.String - Соответствующее значение java.lang.String.
