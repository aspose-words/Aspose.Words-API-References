---
title: "ExportFontFormat"
linktitle: "ExportFontFormat"
second_title: "Aspose.Words para Java"
description: "Indica el formato que se utiliza para exportar fuentes al renderizar en formato HTML fijo en Java."
type: docs
weight: 191
url: /es/java/com.aspose.words/exportfontformat/
---

**Inheritance:**
java.lang.Object
```
public class ExportFontFormat
```

Indica el formato que se usa para exportar fuentes al renderizar a formato HTML fijo.

 **Examples:** 

Muestra cómo usar fuentes solo desde la máquina de destino al guardar un documento en HTML.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [TTF](#TTF) | TTF (formato de fuente TrueType). |
| [WOFF](#WOFF) | WOFF (Formato de Fuente Web Abierta). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String exportFontFormatName)](#fromName-java.lang.String) |  |
| [getName(int exportFontFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int exportFontFormat)](#toString-int) |  |
### TTF {#TTF}
```
public static int TTF
```


TTF (formato de fuente TrueType).

### WOFF {#WOFF}
```
public static int WOFF
```


WOFF (Formato de Fuente Web Abierta).

### length {#length}
```
public static int length
```


### fromName(String exportFontFormatName) {#fromName-java.lang.String}
```
public static int fromName(String exportFontFormatName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| exportFontFormatName | java.lang.String |  |

**Returns:**
int
### getName(int exportFontFormat) {#getName-int}
```
public static String getName(int exportFontFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| exportFontFormat | int |  |

**Returns:**
java.lang.String
