---
title: RtfSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  format.
type: docs
weight: 496
url: /java/com.aspose.words/rtfsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)
```
public class RtfSaveOptions extends SaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.RTF](../../com.aspose.words/saveformat\#RTF) format.

To learn more, visit the **Specify Save Options** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getExportCompactSize()](#getExportCompactSize--) | Allows to make output RTF documents smaller in size, but if they contain RTL (right-to-left) text, it will not be displayed correctly. |
| [setExportCompactSize(boolean value)](#setExportCompactSize-boolean-) | Allows to make output RTF documents smaller in size, but if they contain RTL (right-to-left) text, it will not be displayed correctly. |
| [getExportImagesForOldReaders()](#getExportImagesForOldReaders--) | Specifies whether the keywords for "old readers" are written to RTF or not. |
| [setExportImagesForOldReaders(boolean value)](#setExportImagesForOldReaders-boolean-) | Specifies whether the keywords for "old readers" are written to RTF or not. |
| [getSaveImagesAsWmf()](#getSaveImagesAsWmf--) | When true all images will be saved as WMF. |
| [setSaveImagesAsWmf(boolean value)](#setSaveImagesAsWmf-boolean-) | When true all images will be saved as WMF. |
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.RTF](../../com.aspose.words/saveformat\#RTF).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.RTF](../../com.aspose.words/saveformat\#RTF).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getExportCompactSize() {#getExportCompactSize--}
```
public boolean getExportCompactSize()
```


Allows to make output RTF documents smaller in size, but if they contain RTL (right-to-left) text, it will not be displayed correctly. Default value is  false .

If the document that you want to convert to RTF using Aspose.Words does not contain right-to-left text in languages like Arabic, then you can set this option to  true  to reduce the size of the resulting RTF.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportCompactSize(boolean value) {#setExportCompactSize-boolean-}
```
public void setExportCompactSize(boolean value)
```


Allows to make output RTF documents smaller in size, but if they contain RTL (right-to-left) text, it will not be displayed correctly. Default value is  false .

If the document that you want to convert to RTF using Aspose.Words does not contain right-to-left text in languages like Arabic, then you can set this option to  true  to reduce the size of the resulting RTF.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportImagesForOldReaders() {#getExportImagesForOldReaders--}
```
public boolean getExportImagesForOldReaders()
```


Specifies whether the keywords for "old readers" are written to RTF or not. This can significantly affect the size of the RTF document. Default value is  true .

"Old readers" are pre-Microsoft Word 97 applications and also WordPad. When this option is  true  Aspose.Words writes additional RTF keywords. These keywords allow the document to be displayed correctly when opened in an "old reader" application, but can significantly increase the size of the document.

If you set this option to  false , then only images in WMF, EMF and BMP formats will be displayed in "old readers".

**Returns:**
boolean - The corresponding  boolean  value.
### setExportImagesForOldReaders(boolean value) {#setExportImagesForOldReaders-boolean-}
```
public void setExportImagesForOldReaders(boolean value)
```


Specifies whether the keywords for "old readers" are written to RTF or not. This can significantly affect the size of the RTF document. Default value is  true .

"Old readers" are pre-Microsoft Word 97 applications and also WordPad. When this option is  true  Aspose.Words writes additional RTF keywords. These keywords allow the document to be displayed correctly when opened in an "old reader" application, but can significantly increase the size of the document.

If you set this option to  false , then only images in WMF, EMF and BMP formats will be displayed in "old readers".

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSaveImagesAsWmf() {#getSaveImagesAsWmf--}
```
public boolean getSaveImagesAsWmf()
```


When true all images will be saved as WMF. This option might help to avoid WordPad warning messages.

**Returns:**
boolean - The corresponding  boolean  value.
### setSaveImagesAsWmf(boolean value) {#setSaveImagesAsWmf-boolean-}
```
public void setSaveImagesAsWmf(boolean value)
```


When true all images will be saved as WMF. This option might help to avoid WordPad warning messages.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

