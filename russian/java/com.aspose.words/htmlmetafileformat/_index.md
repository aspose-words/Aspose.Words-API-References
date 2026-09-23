---
title: "HtmlMetafileFormat"
linktitle: "HtmlMetafileFormat"
second_title: "Aspose.Words для Java"
description: "Указывает формат, в котором метафайлы сохраняются в HTML‑документы в Java."
type: docs
weight: 383
url: /ru/java/com.aspose.words/htmlmetafileformat/
---

**Inheritance:**
java.lang.Object
```
public class HtmlMetafileFormat
```

Указывает формат, в котором метафайлы сохраняются в HTML‑документы.

 **Examples:** 

Показывает, как преобразовать объекты SVG в другой формат при сохранении HTML‑документов.

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
## Поля

| Поле | Описание |
| --- | --- |
| [EMF_OR_WMF](#EMF-OR-WMF) | Метафайлы сохраняются как есть, без конвертации. |
| [PNG](#PNG) | Метафайлы рендерятся в растровые изображения PNG. |
| [SVG](#SVG) | Метафайлы конвертируются в векторные изображения SVG. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String htmlMetafileFormatName)](#fromName-java.lang.String) |  |
| [getName(int htmlMetafileFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlMetafileFormat)](#toString-int) |  |
### EMF_OR_WMF {#EMF-OR-WMF}
```
public static int EMF_OR_WMF
```


Метафайлы сохраняются как есть, без конвертации.

### PNG {#PNG}
```
public static int PNG
```


Метафайлы рендерятся в растровые изображения PNG.

### SVG {#SVG}
```
public static int SVG
```


Метафайлы конвертируются в векторные изображения SVG.

### length {#length}
```
public static int length
```


### fromName(String htmlMetafileFormatName) {#fromName-java.lang.String}
```
public static int fromName(String htmlMetafileFormatName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlMetafileFormatName | java.lang.String |  |

**Returns:**
int
### getName(int htmlMetafileFormat) {#getName-int}
```
public static String getName(int htmlMetafileFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlMetafileFormat | int |  |

**Returns:**
java.lang.String
