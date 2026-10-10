---
title: "ExportFontFormat"
linktitle: "ExportFontFormat"
second_title: "Aspose.Words Java için"
description: "Java'da HTML sabit formatına render ederken yazı tiplerini dışa aktarmak için kullanılan formatı gösterir."
type: docs
weight: 191
url: /tr/java/com.aspose.words/exportfontformat/
---

**Inheritance:**
java.lang.Object
```
public class ExportFontFormat
```

HTML sabit formatına render edilirken yazı tiplerini dışa aktarmak için kullanılan biçimi gösterir.

 **Examples:** 

Bir belgeyi HTML olarak kaydederken yalnızca hedef makinedeki yazı tiplerinin nasıl kullanılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [TTF](#TTF) | TTF (TrueType Yazı Tipi formatı). |
| [WOFF](#WOFF) | WOFF (Web Açık Yazı Tipi Formatı). |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String exportFontFormatName)](#fromName-java.lang.String) |  |
| [getName(int exportFontFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int exportFontFormat)](#toString-int) |  |
### TTF {#TTF}
```
public static int TTF
```


TTF (TrueType Yazı Tipi formatı).

### WOFF {#WOFF}
```
public static int WOFF
```


WOFF (Web Açık Yazı Tipi Formatı).

### length {#length}
```
public static int length
```


### fromName(String exportFontFormatName) {#fromName-java.lang.String}
```
public static int fromName(String exportFontFormatName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| exportFontFormatName | java.lang.String |  |

**Returns:**
int
### getName(int exportFontFormat) {#getName-int}
```
public static String getName(int exportFontFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| exportFontFormat | int |  |

**Returns:**
java.lang.String
