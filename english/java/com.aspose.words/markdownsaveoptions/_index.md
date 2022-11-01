---
title: MarkdownSaveOptions
second_title: Aspose.Words for Java API Reference
description: Class to specify additional options when saving a document into the  format.
type: docs
weight: 388
url: /java/com.aspose.words/markdownsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.TxtSaveOptionsBase](../../com.aspose.words/txtsaveoptionsbase)
```
public class MarkdownSaveOptions extends TxtSaveOptionsBase
```

Class to specify additional options when saving a document into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format.

To learn more, visit the **Specify Save Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [MarkdownSaveOptions()](#MarkdownSaveOptions--) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
## Methods

| Method | Description |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int-) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String-) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts--) | Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [getClass()](#getClass--) |  |
| [getDefaultTemplate()](#getDefaultTemplate--) | Gets path to default template (including filename). |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode--) | Gets a value determining how 3D effects are rendered. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | Gets a value determining how DrawingML effects are rendered. |
| [getDmlRenderingMode()](#getDmlRenderingMode--) | Gets a value determining how DrawingML shapes are rendered. |
| [getEncoding()](#getEncoding--) |  |
| [getExportGeneratorName()](#getExportGeneratorName--) | When true, causes the name and version of Aspose.Words to be embedded into produced files. |
| [getExportHeadersFootersMode()](#getExportHeadersFootersMode--) | Specifies the way headers and footers are exported to the text formats. |
| [getExportImagesAsBase64()](#getExportImagesAsBase64--) | Specifies whether images are saved in Base64 format to the output file. |
| [getForcePageBreaks()](#getForcePageBreaks--) | Allows to specify whether the page breaks should be preserved during export. |
| [getImageSavingCallback()](#getImageSavingCallback--) | Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [getImagesFolder()](#getImagesFolder--) | Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [getImlRenderingMode()](#getImlRenderingMode--) | Gets a value determining how ink (InkML) objects are rendered. |
| [getMemoryOptimization()](#getMemoryOptimization--) | Gets value determining if memory optimization should be performed before saving the document. |
| [getParagraphBreak()](#getParagraphBreak--) | Specifies the string to use as a paragraph break when exporting in text formats. |
| [getPrettyFormat()](#getPrettyFormat--) | When  true , pretty formats output where applicable. |
| [getProgressCallback()](#getProgressCallback--) | Called during saving a document and accepts data about saving progress. |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [getTableContentAlignment()](#getTableContentAlignment--) | Gets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [getTempFolder()](#getTempFolder--) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty--) | Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) property is updated before saving. |
| [getUpdateFields()](#getUpdateFields--) | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty--) | Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) property is updated before saving. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty--) | Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) property is updated before saving. |
| [getUpdateSdtContent()](#getUpdateSdtContent--) | Gets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving. |
| [getUseAntiAliasing()](#getUseAntiAliasing--) | Gets a value determining whether or not to use anti-aliasing for rendering. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering--) | Gets a value determining whether or not to use high quality (i.e. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean-) | Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String-) | Sets path to default template (including filename). |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int-) | Sets a value determining how 3D effects are rendered. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | Sets a value determining how DrawingML effects are rendered. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int-) | Sets a value determining how DrawingML shapes are rendered. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) |  |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean-) | When true, causes the name and version of Aspose.Words to be embedded into produced files. |
| [setExportHeadersFootersMode(int value)](#setExportHeadersFootersMode-int-) | Specifies the way headers and footers are exported to the text formats. |
| [setExportImagesAsBase64(boolean value)](#setExportImagesAsBase64-boolean-) | Specifies whether images are saved in Base64 format to the output file. |
| [setForcePageBreaks(boolean value)](#setForcePageBreaks-boolean-) | Allows to specify whether the page breaks should be preserved during export. |
| [setImageSavingCallback(IImageSavingCallback value)](#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) | Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [setImagesFolder(String value)](#setImagesFolder-java.lang.String-) | Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int-) | Sets a value determining how ink (InkML) objects are rendered. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean-) | Sets value determining if memory optimization should be performed before saving the document. |
| [setParagraphBreak(String value)](#setParagraphBreak-java.lang.String-) | Specifies the string to use as a paragraph break when exporting in text formats. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean-) | When  true , pretty formats output where applicable. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback-) | Called during saving a document and accepts data about saving progress. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [setTableContentAlignment(int value)](#setTableContentAlignment-int-) | Sets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean-) | Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) property is updated before saving. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean-) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean-) | Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) property is updated before saving. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean-) | Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) property is updated before saving. |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean-) | Sets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean-) | Sets a value determining whether or not to use anti-aliasing for rendering. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean-) | Sets a value determining whether or not to use high quality (i.e. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### MarkdownSaveOptions() {#MarkdownSaveOptions--}
```
public MarkdownSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format.

### createSaveOptions(int saveFormat) {#createSaveOptions-int-}
```
public static SaveOptions createSaveOptions(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
[SaveOptions](../../com.aspose.words/saveoptions)
### createSaveOptions(String fileName) {#createSaveOptions-java.lang.String-}
```
public static SaveOptions createSaveOptions(String fileName)
```


Creates a save options object of a class suitable for the file extension specified in the given file name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The extension of this file name determines the class of the save options object to create. |

**Returns:**
[SaveOptions](../../com.aspose.words/saveoptions) - An object of a class that derives from [SaveOptions](../../com.aspose.words/saveoptions).
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts--}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**.

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) property is set to  true .

**Returns:**
boolean - A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDefaultTemplate() {#getDefaultTemplate--}
```
public String getDefaultTemplate()
```


Gets path to default template (including filename). Default value for this property is **empty string**. If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-) is true, but [Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) is empty.

**Returns:**
java.lang.String - Path to default template (including filename).
### getDml3DEffectsRenderingMode() {#getDml3DEffectsRenderingMode--}
```
public int getDml3DEffectsRenderingMode()
```


Gets a value determining how 3D effects are rendered. The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**Returns:**
int - A value determining how 3D effects are rendered. The returned value is one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode) constants.
### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode--}
```
public int getDmlEffectsRenderingMode()
```


Gets a value determining how DrawingML effects are rendered. The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

**Returns:**
int - A value determining how DrawingML effects are rendered. The returned value is one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) constants.
### getDmlRenderingMode() {#getDmlRenderingMode--}
```
public int getDmlRenderingMode()
```


Gets a value determining how DrawingML shapes are rendered. The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

This property is used when the document is exported to fixed page formats.

**Returns:**
int - A value determining how DrawingML shapes are rendered. The returned value is one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode) constants.
### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```




**Returns:**
java.nio.charset.Charset
### getExportGeneratorName() {#getExportGeneratorName--}
```
public boolean getExportGeneratorName()
```


When true, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**.

**Returns:**
boolean - The corresponding  boolean  value.
### getExportHeadersFootersMode() {#getExportHeadersFootersMode--}
```
public int getExportHeadersFootersMode()
```


Specifies the way headers and footers are exported to the text formats. Default value is [TxtExportHeadersFootersMode.PRIMARY\_ONLY](../../com.aspose.words/txtexportheadersfootersmode\#PRIMARY-ONLY).

**Returns:**
int - The corresponding  int  value. The returned value is one of [TxtExportHeadersFootersMode](../../com.aspose.words/txtexportheadersfootersmode) constants.
### getExportImagesAsBase64() {#getExportImagesAsBase64--}
```
public boolean getExportImagesAsBase64()
```


Specifies whether images are saved in Base64 format to the output file. Default is  false .

When this property is set to  true  images data are exported directly into the **img** elements and separate files are not created.

**Returns:**
boolean - The corresponding  boolean  value.
### getForcePageBreaks() {#getForcePageBreaks--}
```
public boolean getForcePageBreaks()
```


Allows to specify whether the page breaks should be preserved during export.

The default value is **false**.

The property affects only page breaks that are inserted explicitly into a document. It is not related to page breaks that MS Word automatically inserts at the end of each page.

**Returns:**
boolean - The corresponding  boolean  value.
### getImageSavingCallback() {#getImageSavingCallback--}
```
public IImageSavingCallback getImageSavingCallback()
```


Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format.

**Returns:**
[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) - The corresponding [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) value.
### getImagesFolder() {#getImagesFolder--}
```
public String getImagesFolder()
```


Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) property.

If the folder specified by [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) doesn't exist, it will be created automatically.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getImlRenderingMode() {#getImlRenderingMode--}
```
public int getImlRenderingMode()
```


Gets a value determining how ink (InkML) objects are rendered. The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

This property is used when the document is exported to fixed page formats.

**Returns:**
int - A value determining how ink (InkML) objects are rendered. The returned value is one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode) constants.
### getMemoryOptimization() {#getMemoryOptimization--}
```
public boolean getMemoryOptimization()
```


Gets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. Setting this option to true can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

**Returns:**
boolean - Value determining if memory optimization should be performed before saving the document.
### getParagraphBreak() {#getParagraphBreak--}
```
public String getParagraphBreak()
```


Specifies the string to use as a paragraph break when exporting in text formats.

The default value is [ControlChar.CR\_LF](../../com.aspose.words/controlchar\#CR-LF).

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getPrettyFormat() {#getPrettyFormat--}
```
public boolean getPrettyFormat()
```


When  true , pretty formats output where applicable. Default value is **false**.

Set to **true** to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

**Returns:**
boolean - The corresponding  boolean  value.
### getProgressCallback() {#getProgressCallback--}
```
public IDocumentSavingCallback getProgressCallback()
```


Called during saving a document and accepts data about saving progress.

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**Returns:**
[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) - The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) value.
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### getTableContentAlignment() {#getTableContentAlignment--}
```
public int getTableContentAlignment()
```


Gets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. The default value is [TableContentAlignment.AUTO](../../com.aspose.words/tablecontentalignment\#AUTO).

**Returns:**
int - A value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. The returned value is one of [TableContentAlignment](../../com.aspose.words/tablecontentalignment) constants.
### getTempFolder() {#getTempFolder--}
```
public String getTempFolder()
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

When Aspose.Words saves a document, it needs to create temporary internal structures. By default, these internal structures are created in memory and the memory usage spikes for a short period while the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

If you are saving a very large document (thousands of pages) and/or processing many documents at the same time, then the memory spike during saving can be significant enough to cause the system to throw java.lang.IndexOutOfBoundsException. Specifying a temporary folder using [getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-) will cause Aspose.Words to keep the internal structures in temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getUpdateCreatedTimeProperty() {#getUpdateCreatedTimeProperty--}
```
public boolean getUpdateCreatedTimeProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) property is updated before saving. Default value is false;

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) property is updated before saving.
### getUpdateFields() {#getUpdateFields--}
```
public boolean getUpdateFields()
```


Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. Allows to specify whether to mimic or not MS Word behavior.

**Returns:**
boolean - A value determining if fields of certain types should be updated before saving the document to a fixed page format.
### getUpdateLastPrintedProperty() {#getUpdateLastPrintedProperty--}
```
public boolean getUpdateLastPrintedProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) property is updated before saving.

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) property is updated before saving.
### getUpdateLastSavedTimeProperty() {#getUpdateLastSavedTimeProperty--}
```
public boolean getUpdateLastSavedTimeProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) property is updated before saving.

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) property is updated before saving.
### getUpdateSdtContent() {#getUpdateSdtContent--}
```
public boolean getUpdateSdtContent()
```


Gets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving. The default value is  false .

**Returns:**
boolean - Value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving.
### getUseAntiAliasing() {#getUseAntiAliasing--}
```
public boolean getUseAntiAliasing()
```


Gets a value determining whether or not to use anti-aliasing for rendering.

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) and [SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) formats this option is used for raster images.

**Returns:**
boolean - A value determining whether or not to use anti-aliasing for rendering.
### getUseHighQualityRendering() {#getUseHighQualityRendering--}
```
public boolean getUseHighQualityRendering()
```


Gets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**Returns:**
boolean - A value determining whether or not to use high quality (i.e.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAllowEmbeddingPostScriptFonts(boolean value) {#setAllowEmbeddingPostScriptFonts-boolean-}
```
public void setAllowEmbeddingPostScriptFonts(boolean value)
```


Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**.

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) property is set to  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String-}
```
public void setDefaultTemplate(String value)
```


Sets path to default template (including filename). Default value for this property is **empty string**. If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-) is true, but [Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) is empty.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Path to default template (including filename). |

### setDml3DEffectsRenderingMode(int value) {#setDml3DEffectsRenderingMode-int-}
```
public void setDml3DEffectsRenderingMode(int value)
```


Sets a value determining how 3D effects are rendered. The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how 3D effects are rendered. The value must be one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode) constants. |

### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int-}
```
public void setDmlEffectsRenderingMode(int value)
```


Sets a value determining how DrawingML effects are rendered. The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML effects are rendered. The value must be one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) constants. |

### setDmlRenderingMode(int value) {#setDmlRenderingMode-int-}
```
public void setDmlRenderingMode(int value)
```


Sets a value determining how DrawingML shapes are rendered. The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

This property is used when the document is exported to fixed page formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML shapes are rendered. The value must be one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode) constants. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset-}
```
public void setEncoding(Charset value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.nio.charset.Charset |  |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean-}
```
public void setExportGeneratorName(boolean value)
```


When true, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportHeadersFootersMode(int value) {#setExportHeadersFootersMode-int-}
```
public void setExportHeadersFootersMode(int value)
```


Specifies the way headers and footers are exported to the text formats. Default value is [TxtExportHeadersFootersMode.PRIMARY\_ONLY](../../com.aspose.words/txtexportheadersfootersmode\#PRIMARY-ONLY).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TxtExportHeadersFootersMode](../../com.aspose.words/txtexportheadersfootersmode) constants. |

### setExportImagesAsBase64(boolean value) {#setExportImagesAsBase64-boolean-}
```
public void setExportImagesAsBase64(boolean value)
```


Specifies whether images are saved in Base64 format to the output file. Default is  false .

When this property is set to  true  images data are exported directly into the **img** elements and separate files are not created.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setForcePageBreaks(boolean value) {#setForcePageBreaks-boolean-}
```
public void setForcePageBreaks(boolean value)
```


Allows to specify whether the page breaks should be preserved during export.

The default value is **false**.

The property affects only page breaks that are inserted explicitly into a document. It is not related to page breaks that MS Word automatically inserts at the end of each page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setImageSavingCallback(IImageSavingCallback value) {#setImageSavingCallback-com.aspose.words.IImageSavingCallback-}
```
public void setImageSavingCallback(IImageSavingCallback value)
```


Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) | The corresponding [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) value. |

### setImagesFolder(String value) {#setImagesFolder-java.lang.String-}
```
public void setImagesFolder(String value)
```


Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) property.

If the folder specified by [getImagesFolder()](../../com.aspose.words/markdownsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions\#setImagesFolder-java.lang.String-) doesn't exist, it will be created automatically.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setImlRenderingMode(int value) {#setImlRenderingMode-int-}
```
public void setImlRenderingMode(int value)
```


Sets a value determining how ink (InkML) objects are rendered. The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

This property is used when the document is exported to fixed page formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how ink (InkML) objects are rendered. The value must be one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode) constants. |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean-}
```
public void setMemoryOptimization(boolean value)
```


Sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. Setting this option to true can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining if memory optimization should be performed before saving the document. |

### setParagraphBreak(String value) {#setParagraphBreak-java.lang.String-}
```
public void setParagraphBreak(String value)
```


Specifies the string to use as a paragraph break when exporting in text formats.

The default value is [ControlChar.CR\_LF](../../com.aspose.words/controlchar\#CR-LF).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setPrettyFormat(boolean value) {#setPrettyFormat-boolean-}
```
public void setPrettyFormat(boolean value)
```


When  true , pretty formats output where applicable. Default value is **false**.

Set to **true** to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setProgressCallback(IDocumentSavingCallback value) {#setProgressCallback-com.aspose.words.IDocumentSavingCallback-}
```
public void setProgressCallback(IDocumentSavingCallback value)
```


Called during saving a document and accepts data about saving progress.

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) | The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) value. |

### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### setTableContentAlignment(int value) {#setTableContentAlignment-int-}
```
public void setTableContentAlignment(int value)
```


Sets a value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. The default value is [TableContentAlignment.AUTO](../../com.aspose.words/tablecontentalignment\#AUTO).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value that specifies how to align contents in tables when exporting into the [SaveFormat.MARKDOWN](../../com.aspose.words/saveformat\#MARKDOWN) format. The value must be one of [TableContentAlignment](../../com.aspose.words/tablecontentalignment) constants. |

### setTempFolder(String value) {#setTempFolder-java.lang.String-}
```
public void setTempFolder(String value)
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

When Aspose.Words saves a document, it needs to create temporary internal structures. By default, these internal structures are created in memory and the memory usage spikes for a short period while the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

If you are saving a very large document (thousands of pages) and/or processing many documents at the same time, then the memory spike during saving can be significant enough to cause the system to throw java.lang.IndexOutOfBoundsException. Specifying a temporary folder using [getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-) will cause Aspose.Words to keep the internal structures in temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setUpdateCreatedTimeProperty(boolean value) {#setUpdateCreatedTimeProperty-boolean-}
```
public void setUpdateCreatedTimeProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) property is updated before saving. Default value is false;

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) property is updated before saving. |

### setUpdateFields(boolean value) {#setUpdateFields-boolean-}
```
public void setUpdateFields(boolean value)
```


Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. Allows to specify whether to mimic or not MS Word behavior.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining if fields of certain types should be updated before saving the document to a fixed page format. |

### setUpdateLastPrintedProperty(boolean value) {#setUpdateLastPrintedProperty-boolean-}
```
public void setUpdateLastPrintedProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) property is updated before saving.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) property is updated before saving. |

### setUpdateLastSavedTimeProperty(boolean value) {#setUpdateLastSavedTimeProperty-boolean-}
```
public void setUpdateLastSavedTimeProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) property is updated before saving.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) property is updated before saving. |

### setUpdateSdtContent(boolean value) {#setUpdateSdtContent-boolean-}
```
public void setUpdateSdtContent(boolean value)
```


Sets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) is updated before saving. |

### setUseAntiAliasing(boolean value) {#setUseAntiAliasing-boolean-}
```
public void setUseAntiAliasing(boolean value)
```


Sets a value determining whether or not to use anti-aliasing for rendering.

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) and [SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) formats this option is used for raster images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use anti-aliasing for rendering. |

### setUseHighQualityRendering(boolean value) {#setUseHighQualityRendering-boolean-}
```
public void setUseHighQualityRendering(boolean value)
```


Sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use high quality (i.e. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

