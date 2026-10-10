---
title: "ExportFontFormat"
linktitle: "ExportFontFormat"
second_title: "Aspose.Words für Java"
description: "Gibt das Format an, das zum Exportieren von Schriftarten beim Rendern in das feste HTML-Format in Java verwendet wird."
type: docs
weight: 191
url: /de/java/com.aspose.words/exportfontformat/
---

**Inheritance:**
java.lang.Object
```
public class ExportFontFormat
```

Gibt das Format an, das zum Exportieren von Schriftarten beim Rendern in das feste HTML-Format verwendet wird.

 **Examples:** 

Zeigt, wie man beim Speichern eines Dokuments als HTML nur Schriftarten vom Zielrechner verwendet.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [TTF](#TTF) | TTF (TrueType-Schriftformat). |
| [WOFF](#WOFF) | WOFF (Web Open Font Format). |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String exportFontFormatName)](#fromName-java.lang.String) |  |
| [getName(int exportFontFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int exportFontFormat)](#toString-int) |  |
### TTF {#TTF}
```
public static int TTF
```


TTF (TrueType-Schriftformat).

### WOFF {#WOFF}
```
public static int WOFF
```


WOFF (Web Open Font Format).

### length {#length}
```
public static int length
```


### fromName(String exportFontFormatName) {#fromName-java.lang.String}
```
public static int fromName(String exportFontFormatName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| exportFontFormatName | java.lang.String |  |

**Returns:**
int
### getName(int exportFontFormat) {#getName-int}
```
public static String getName(int exportFontFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| exportFontFormat | int |  |

**Returns:**
java.lang.String
