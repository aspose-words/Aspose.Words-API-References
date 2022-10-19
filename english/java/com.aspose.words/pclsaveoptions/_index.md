---
title: PclSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  format.
type: docs
weight: 448
url: /java/com.aspose.words/pclsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)
```
public class PclSaveOptions extends FixedPageSaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.PCL](../../com.aspose.words/saveformat\#PCL) format.

To learn more, visit the **Specify Save Options** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getRasterizeTransformedElements()](#getRasterizeTransformedElements--) | Gets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document. |
| [setRasterizeTransformedElements(boolean value)](#setRasterizeTransformedElements-boolean-) | Sets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document. |
| [addPrinterFont(String fontFullName, String fontPclName)](#addPrinterFont-java.lang.String-java.lang.String-) | Adds information about font that is uploaded to the printer by manufacturer. |
| [getFallbackFontName()](#getFallbackFontName--) | Name of the font that will be used if no expected font is found in printer and built-in fonts collections. |
| [setFallbackFontName(String value)](#setFallbackFontName-java.lang.String-) | Name of the font that will be used if no expected font is found in printer and built-in fonts collections. |
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.PCL](../../com.aspose.words/saveformat\#PCL).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.PCL](../../com.aspose.words/saveformat\#PCL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getRasterizeTransformedElements() {#getRasterizeTransformedElements--}
```
public boolean getRasterizeTransformedElements()
```


Gets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document. Default is  true . PCL doesn't support some kind of transformations that are used by Aspose Words. E.g. rotated, skewed images and texture brushes. To properly render such elements rasterization process is used, i.e. saving to image and clipping. This process can take additional time and memory. If flag is set to  false , some content in output may be different as compared with the source document.

**Returns:**
boolean - A value determining whether or not complex transformed elements should be rasterized before saving to PCL document.
### setRasterizeTransformedElements(boolean value) {#setRasterizeTransformedElements-boolean-}
```
public void setRasterizeTransformedElements(boolean value)
```


Sets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document. Default is  true . PCL doesn't support some kind of transformations that are used by Aspose Words. E.g. rotated, skewed images and texture brushes. To properly render such elements rasterization process is used, i.e. saving to image and clipping. This process can take additional time and memory. If flag is set to  false , some content in output may be different as compared with the source document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not complex transformed elements should be rasterized before saving to PCL document. |

### addPrinterFont(String fontFullName, String fontPclName) {#addPrinterFont-java.lang.String-java.lang.String-}
```
public void addPrinterFont(String fontFullName, String fontPclName)
```


Adds information about font that is uploaded to the printer by manufacturer.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontFullName | java.lang.String | Full name of the font (e.g. "Times New Roman Bold Italic"). |
| fontPclName | java.lang.String | Name of the font that is used in Pcl document. There are 52 fonts that are to be built in any printer according to Pcl specification. However manufactures can add some other fonts to their devices. |

### getFallbackFontName() {#getFallbackFontName--}
```
public String getFallbackFontName()
```


Name of the font that will be used if no expected font is found in printer and built-in fonts collections. If no fallback is found, a warning is generated and "Arial" font is used.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setFallbackFontName(String value) {#setFallbackFontName-java.lang.String-}
```
public void setFallbackFontName(String value)
```


Name of the font that will be used if no expected font is found in printer and built-in fonts collections. If no fallback is found, a warning is generated and "Arial" font is used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

