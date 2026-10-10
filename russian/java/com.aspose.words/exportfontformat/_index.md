---
title: "ExportFontFormat"
linktitle: "ExportFontFormat"
second_title: "Aspose.Words для Java"
description: "Указывает формат, используемый для экспорта шрифтов при рендеринге в фиксированный формат HTML на Java."
type: docs
weight: 191
url: /ru/java/com.aspose.words/exportfontformat/
---

**Inheritance:**
java.lang.Object
```
public class ExportFontFormat
```

Указывает формат, используемый для экспорта шрифтов при рендеринге в фиксированный формат HTML.

 **Examples:** 

Показывает, как использовать шрифты только с целевой машины при сохранении документа в HTML.

```

 Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setExportEmbeddedCss(true);
     saveOptions.setUseTargetMachineFonts(useTargetMachineFonts);
     saveOptions.setFontFormat(ExportFontFormat.TTF);
     saveOptions.setExportEmbeddedFonts(false);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html"), StandardCharsets.UTF_8);

 if (useTargetMachineFonts)
     Assert.assertFalse(Pattern.compile("@font-face").matcher(outDocContents).find());
 else
     Assert.assertTrue(Pattern.compile(
         "@font-face [{] font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'\u263a'[)], " +
         "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; [}]").matcher(outDocContents).find());
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [TTF](#TTF) | TTF (формат шрифта TrueType). |
| [WOFF](#WOFF) | WOFF (формат веб‑открытых шрифтов). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String exportFontFormatName)](#fromName-java.lang.String) |  |
| [getName(int exportFontFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int exportFontFormat)](#toString-int) |  |
### TTF {#TTF}
```
public static int TTF
```


TTF (формат шрифта TrueType).

### WOFF {#WOFF}
```
public static int WOFF
```


WOFF (формат веб‑открытых шрифтов).

### length {#length}
```
public static int length
```


### fromName(String exportFontFormatName) {#fromName-java.lang.String}
```
public static int fromName(String exportFontFormatName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| exportFontFormatName | java.lang.String |  |

**Returns:**
int
### getName(int exportFontFormat) {#getName-int}
```
public static String getName(int exportFontFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| exportFontFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int exportFontFormat) {#toString-int}
```
public static String toString(int exportFontFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| exportFontFormat | int |  |

**Returns:**
java.lang.String
