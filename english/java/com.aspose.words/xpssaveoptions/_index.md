---
title: XpsSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  format.
type: docs
weight: 630
url: /java/com.aspose.words/xpssaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)
```
public class XpsSaveOptions extends FixedPageSaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.XPS](../../com.aspose.words/saveformat\#XPS) format.

To learn more, visit the **Specify Save Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [XpsSaveOptions()](#XpsSaveOptions--) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XPS](../../com.aspose.words/saveformat\#XPS) format. |
| [XpsSaveOptions(int saveFormat)](#XpsSaveOptions-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getOutlineOptions()](#getOutlineOptions--) | Allows to specify outline options. |
| [getUseBookFoldPrintingSettings()](#getUseBookFoldPrintingSettings--) | Gets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |
| [setUseBookFoldPrintingSettings(boolean value)](#setUseBookFoldPrintingSettings-boolean-) | Sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |
### XpsSaveOptions() {#XpsSaveOptions--}
```
public XpsSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XPS](../../com.aspose.words/saveformat\#XPS) format.

### XpsSaveOptions(int saveFormat) {#XpsSaveOptions-int-}
```
public XpsSaveOptions(int saveFormat)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XPS](../../com.aspose.words/saveformat\#XPS).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XPS](../../com.aspose.words/saveformat\#XPS).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getOutlineOptions() {#getOutlineOptions--}
```
public OutlineOptions getOutlineOptions()
```


Allows to specify outline options.

Note that ExpandedOutlineLevels option will not work when saving to XPS.

**Returns:**
[OutlineOptions](../../com.aspose.words/outlineoptions) - The corresponding [OutlineOptions](../../com.aspose.words/outlineoptions) value.
### getUseBookFoldPrintingSettings() {#getUseBookFoldPrintingSettings--}
```
public boolean getUseBookFoldPrintingSettings()
```


Gets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-).

If this option is specified, [FixedPageSaveOptions.getPageSet()](../../com.aspose.words/fixedpagesaveoptions\#getPageSet--) / [FixedPageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/fixedpagesaveoptions\#setPageSet-com.aspose.words.PageSet-) is ignored when saving. This behavior matches MS Word. If book fold printing settings are not specified in page setup, this option will have no effect.

**Returns:**
boolean - A boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-).
### setUseBookFoldPrintingSettings(boolean value) {#setUseBookFoldPrintingSettings-boolean-}
```
public void setUseBookFoldPrintingSettings(boolean value)
```


Sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-).

If this option is specified, [FixedPageSaveOptions.getPageSet()](../../com.aspose.words/fixedpagesaveoptions\#getPageSet--) / [FixedPageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/fixedpagesaveoptions\#setPageSet-com.aspose.words.PageSet-) is ignored when saving. This behavior matches MS Word. If book fold printing settings are not specified in page setup, this option will have no effect.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |

