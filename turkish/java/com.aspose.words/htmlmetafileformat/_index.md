---
title: "HtmlMetafileFormat"
linktitle: "HtmlMetafileFormat"
second_title: "Aspose.Words Java için"
description: "Metafile'lerin Java'da HTML belgelerine kaydedildiği formatı gösterir."
type: docs
weight: 383
url: /tr/java/com.aspose.words/htmlmetafileformat/
---

**Inheritance:**
java.lang.Object
```
public class HtmlMetafileFormat
```

Metadosyaların HTML belgelerine kaydedildiği biçimi gösterir.

 **Examples:** 

HTML belgeleri kaydedilirken SVG nesnelerinin farklı bir formata nasıl dönüştürüleceğini gösterir.

```

 String html =
     "\n                    \n                        Hello world!\n                    \n                ";

 // Use 'ConvertSvgToEmf' to turn back the legacy behavior
 // where all SVG images loaded from an HTML document were converted to EMF.
 // Now SVG images are loaded without conversion
 // if the MS Word version specified in load options supports SVG images natively.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(); { loadOptions.setConvertSvgToEmf(true); }

 Document doc = new Document(new ByteArrayInputStream(html.getBytes()));

 // This document contains a  element in the form of text.
 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles this object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Png" to convert it to a PNG image.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Svg" preserve it as a SVG object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.EmfOrWmf" to convert it to a metafile.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setMetafileFormat(htmlMetafileFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html"), StandardCharsets.UTF_8);

 switch (htmlMetafileFormat) {
     case HtmlMetafileFormat.PNG:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
     case HtmlMetafileFormat.SVG:
         Assert.assertTrue(outDocContents.contains(
                 "" +
                         ""));
         break;
     case HtmlMetafileFormat.EMF_OR_WMF:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
 }
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [EMF_OR_WMF](#EMF-OR-WMF) | Metafile'ler olduğu gibi, dönüşüm olmadan kaydedilir. |
| [PNG](#PNG) | Metafile'ler raster PNG görüntülerine işlenir. |
| [SVG](#SVG) | Metafile'ler vektör SVG görüntülerine dönüştürülür. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String htmlMetafileFormatName)](#fromName-java.lang.String) |  |
| [getName(int htmlMetafileFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlMetafileFormat)](#toString-int) |  |
### EMF_OR_WMF {#EMF-OR-WMF}
```
public static int EMF_OR_WMF
```


Metafile'ler olduğu gibi, dönüşüm olmadan kaydedilir.

### PNG {#PNG}
```
public static int PNG
```


Metafile'ler raster PNG görüntülerine işlenir.

### SVG {#SVG}
```
public static int SVG
```


Metafile'ler vektör SVG görüntülerine dönüştürülür.

### length {#length}
```
public static int length
```


### fromName(String htmlMetafileFormatName) {#fromName-java.lang.String}
```
public static int fromName(String htmlMetafileFormatName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlMetafileFormatName | java.lang.String |  |

**Returns:**
int
### getName(int htmlMetafileFormat) {#getName-int}
```
public static String getName(int htmlMetafileFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlMetafileFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlMetafileFormat) {#toString-int}
```
public static String toString(int htmlMetafileFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlMetafileFormat | int |  |

**Returns:**
java.lang.String
