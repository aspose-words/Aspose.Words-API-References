---
title: CssSavingArgs
second_title: Aspose.Words for Java API Reference
description: Provides data for the  event.
type: docs
weight: 96
url: /java/com.aspose.words/csssavingargs/
---

**Inheritance:**
java.lang.Object
```
public class CssSavingArgs
```

Provides data for the [ICssSavingCallback.cssSaving(com.aspose.words.CssSavingArgs)](../../com.aspose.words/icsssavingcallback\#cssSaving-com.aspose.words.CssSavingArgs-) event.

To learn more, visit the **Save a Document** documentation article.

By default, when Aspose.Words saves a document to HTML, it saves CSS information inline (as a value of the **style** attribute on every element).

[CssSavingArgs](../../com.aspose.words/csssavingargs) allows to save CSS information into file by providing your own stream object.

To save CSS into stream, use the **P:Aspose.Words.Saving.CssSavingArgs.CssStream** property.

To suppress saving CSS into a file and embedding to HTML document use the [isExportNeeded()](../../com.aspose.words/csssavingargs\#isExportNeeded--) / [isExportNeeded(boolean)](../../com.aspose.words/csssavingargs\#isExportNeeded-boolean-) property.
## Methods

| Method | Description |
| --- | --- |
| [getDocument()](#getDocument--) | Gets the document object that is currently being saved. |
| [getKeepCssStreamOpen()](#getKeepCssStreamOpen--) | Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information. |
| [setKeepCssStreamOpen(boolean value)](#setKeepCssStreamOpen-boolean-) | Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information. |
| [getCssStream()](#getCssStream--) |  |
| [setCssStream(OutputStream value)](#setCssStream-java.io.OutputStream-) |  |
| [isExportNeeded()](#isExportNeeded--) | Allows to specify whether the CSS will be exported to file and embedded to HTML document. |
| [isExportNeeded(boolean value)](#isExportNeeded-boolean-) | Allows to specify whether the CSS will be exported to file and embedded to HTML document. |
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Gets the document object that is currently being saved.

**Returns:**
[Document](../../com.aspose.words/document) - The document object that is currently being saved.
### getKeepCssStreamOpen() {#getKeepCssStreamOpen--}
```
public boolean getKeepCssStreamOpen()
```


Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information.

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.CssSavingArgs.CssStream** property after writing an CSS information into it. Specify  true  to keep the stream open.

**P:Aspose.Words.Saving.CssSavingArgs.CssStream**

**Returns:**
boolean - The corresponding  boolean  value.
### setKeepCssStreamOpen(boolean value) {#setKeepCssStreamOpen-boolean-}
```
public void setKeepCssStreamOpen(boolean value)
```


Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information.

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.CssSavingArgs.CssStream** property after writing an CSS information into it. Specify  true  to keep the stream open.

**P:Aspose.Words.Saving.CssSavingArgs.CssStream**

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getCssStream() {#getCssStream--}
```
public OutputStream getCssStream()
```




**Returns:**
java.io.OutputStream
### setCssStream(OutputStream value) {#setCssStream-java.io.OutputStream-}
```
public void setCssStream(OutputStream value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### isExportNeeded() {#isExportNeeded--}
```
public boolean isExportNeeded()
```


Allows to specify whether the CSS will be exported to file and embedded to HTML document. Default is  true . When this property is  false , the CSS information will not be saved to a CSS file and will not be embedded to HTML document.

**Returns:**
boolean - The corresponding  boolean  value.
### isExportNeeded(boolean value) {#isExportNeeded-boolean-}
```
public void isExportNeeded(boolean value)
```


Allows to specify whether the CSS will be exported to file and embedded to HTML document. Default is  true . When this property is  false , the CSS information will not be saved to a CSS file and will not be embedded to HTML document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |
