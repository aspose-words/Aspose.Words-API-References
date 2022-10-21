---
title: PsSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  format.
type: docs
weight: 471
url: /java/com.aspose.words/pssaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)
```
public class PsSaveOptions extends FixedPageSaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.PS](../../com.aspose.words/saveformat\#PS) format.

To learn more, visit the **Specify Save Options** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getUseBookFoldPrintingSettings()](#getUseBookFoldPrintingSettings--) | Gets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |
| [setUseBookFoldPrintingSettings(boolean value)](#setUseBookFoldPrintingSettings-boolean-) | Sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.PS](../../com.aspose.words/saveformat\#PS).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.PS](../../com.aspose.words/saveformat\#PS).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

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

