---
title: PdfSaveOptions
linktitle: PdfSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the SaveFormat.PDF format in Java.
type: docs
weight: 468
url: /java/com.aspose.words/pdfsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions/), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class PdfSaveOptions extends FixedPageSaveOptions implements Cloneable
```

Can be used to specify additional options when saving a document into the [SaveFormat.PDF](../../com.aspose.words/saveformat/\#PDF) format.

To learn more, visit the [ Specify Save Options ][Specify Save Options] documentation article.


[Specify Save Options]: https://docs.aspose.com/words/java/specify-save-options/
## Constructors

| Constructor | Description |
| --- | --- |
| [PdfSaveOptions()](#PdfSaveOptions) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.PDF](../../com.aspose.words/saveformat/\#PDF) format. |
## Methods

| Method | Description |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [deepClone()](#deepClone) | Creates a deep clone of this object. |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [getAdditionalTextPositioning()](#getAdditionalTextPositioning) | A flag specifying whether to write additional text positioning operators or not. |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts) | Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [getCacheBackgroundGraphics()](#getCacheBackgroundGraphics) | Gets a value determining whether or not to cache graphics placed in document's background. |
| [getClass()](#getClass) |  |
| [getColorMode()](#getColorMode) | Gets a value determining how colors are rendered. |
| [getCompliance()](#getCompliance) | Specifies the PDF standards compliance level for output documents. |
| [getCreateNoteHyperlinks()](#getCreateNoteHyperlinks) | Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. |
| [getCustomPropertiesExport()](#getCustomPropertiesExport) | Gets a value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) are exported to PDF file. |
| [getDefaultTemplate()](#getDefaultTemplate) | Gets path to default template (including filename). |
| [getDigitalSignatureDetails()](#getDigitalSignatureDetails) | Gets the details for signing the output PDF document. |
| [getDisplayDocTitle()](#getDisplayDocTitle) | A flag specifying whether the window\\u2019s title bar should display the document title taken from the Title entry of the document information dictionary. |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode) | Gets a value determining how 3D effects are rendered. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode) | Gets a value determining how DrawingML effects are rendered. |
| [getDmlRenderingMode()](#getDmlRenderingMode) | Gets a value determining how DrawingML shapes are rendered. |
| [getDownsampleOptions()](#getDownsampleOptions) | Allows to specify downsample options. |
| [getEmbedAttachments()](#getEmbedAttachments) | Gets a value determining whether or not to embed attachments to the PDF document. |
| [getEmbedFullFonts()](#getEmbedFullFonts) | Controls how fonts are embedded into the resulting PDF documents. |
| [getEncryptionDetails()](#getEncryptionDetails) | Gets the details for encrypting the output PDF document. |
| [getExportDocumentStructure()](#getExportDocumentStructure) | Gets a value determining whether or not to export document structure. |
| [getExportGeneratorName()](#getExportGeneratorName) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [getExportLanguageToSpanTag()](#getExportLanguageToSpanTag) | Gets a value determining whether or not to create a "Span" tag in the document structure to export the text language. |
| [getFontEmbeddingMode()](#getFontEmbeddingMode) | Specifies the font embedding mode. |
| [getHeaderFooterBookmarksExportMode()](#getHeaderFooterBookmarksExportMode) | Determines how bookmarks in headers/footers are exported. |
| [getImageColorSpaceExportMode()](#getImageColorSpaceExportMode) | Specifies how the color space will be selected for the images in PDF document. |
| [getImageCompression()](#getImageCompression) | Specifies compression type to be used for all images in the document. |
| [getImlRenderingMode()](#getImlRenderingMode) | Gets a value determining how ink (InkML) objects are rendered. |
| [getInterpolateImages()](#getInterpolateImages) | A flag indicating whether image interpolation shall be performed by a conforming reader. |
| [getJpegQuality()](#getJpegQuality) | Gets a value determining the quality of the JPEG images inside PDF document. |
| [getMemoryOptimization()](#getMemoryOptimization) | Gets value determining if memory optimization should be performed before saving the document. |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions) | Allows to specify metafile rendering options. |
| [getNumeralFormat()](#getNumeralFormat) | Gets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. |
| [getOpenHyperlinksInNewWindow()](#getOpenHyperlinksInNewWindow) | Gets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |
| [getOptimizeOutput()](#getOptimizeOutput) | Flag indicates whether it is required to optimize output. |
| [getOutlineOptions()](#getOutlineOptions) | Allows to specify outline options. |
| [getPageMode()](#getPageMode) | Specifies how the PDF document should be displayed when opened in the PDF reader. |
| [getPageSavingCallback()](#getPageSavingCallback) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [getPageSet()](#getPageSet) | Gets the pages to render. |
| [getPreblendImages()](#getPreblendImages) | Gets a value determining whether or not to preblend transparent images with black background color. |
| [getPreserveFormFields()](#getPreserveFormFields) | Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. |
| [getPrettyFormat()](#getPrettyFormat) | When  true , pretty formats output where applicable. |
| [getProgressCallback()](#getProgressCallback) | Called during saving a document and accepts data about saving progress. |
| [getSaveFormat()](#getSaveFormat) | Specifies the format in which the document will be saved if this save options object is used. |
| [getTempFolder()](#getTempFolder) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [getTextCompression()](#getTextCompression) | Specifies compression type to be used for all textual content in the document. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [getUpdateFields()](#getUpdateFields) | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [getUpdateSdtContent()](#getUpdateSdtContent) | Gets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving. |
| [getUseAntiAliasing()](#getUseAntiAliasing) | Gets a value determining whether or not to use anti-aliasing for rendering. |
| [getUseBookFoldPrintingSettings()](#getUseBookFoldPrintingSettings) | Gets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int). |
| [getUseCoreFonts()](#getUseCoreFonts) | Gets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering) | Gets a value determining whether or not to use high quality (i.e. |
| [getZoomBehavior()](#getZoomBehavior) | Gets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. |
| [getZoomFactor()](#getZoomFactor) | Gets a value determining zoom factor (in percentages) for a document. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setAdditionalTextPositioning(boolean value)](#setAdditionalTextPositioning-boolean) | A flag specifying whether to write additional text positioning operators or not. |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean) | Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [setCacheBackgroundGraphics(boolean value)](#setCacheBackgroundGraphics-boolean) | Sets a value determining whether or not to cache graphics placed in document's background. |
| [setColorMode(int value)](#setColorMode-int) | Sets a value determining how colors are rendered. |
| [setCompliance(int value)](#setCompliance-int) | Specifies the PDF standards compliance level for output documents. |
| [setCreateNoteHyperlinks(boolean value)](#setCreateNoteHyperlinks-boolean) | Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. |
| [setCustomPropertiesExport(int value)](#setCustomPropertiesExport-int) | Sets a value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) are exported to PDF file. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String) | Sets path to default template (including filename). |
| [setDigitalSignatureDetails(PdfDigitalSignatureDetails value)](#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails) | Sets the details for signing the output PDF document. |
| [setDisplayDocTitle(boolean value)](#setDisplayDocTitle-boolean) | A flag specifying whether the window\\u2019s title bar should display the document title taken from the Title entry of the document information dictionary. |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int) | Sets a value determining how 3D effects are rendered. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int) | Sets a value determining how DrawingML effects are rendered. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int) | Sets a value determining how DrawingML shapes are rendered. |
| [setDownsampleOptions(DownsampleOptions value)](#setDownsampleOptions-com.aspose.words.DownsampleOptions) | Allows to specify downsample options. |
| [setEmbedAttachments(boolean value)](#setEmbedAttachments-boolean) | Sets a value determining whether or not to embed attachments to the PDF document. |
| [setEmbedFullFonts(boolean value)](#setEmbedFullFonts-boolean) | Controls how fonts are embedded into the resulting PDF documents. |
| [setEncryptionDetails(PdfEncryptionDetails value)](#setEncryptionDetails-com.aspose.words.PdfEncryptionDetails) | Sets the details for encrypting the output PDF document. |
| [setExportDocumentStructure(boolean value)](#setExportDocumentStructure-boolean) | Sets a value determining whether or not to export document structure. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [setExportLanguageToSpanTag(boolean value)](#setExportLanguageToSpanTag-boolean) | Sets a value determining whether or not to create a "Span" tag in the document structure to export the text language. |
| [setFontEmbeddingMode(int value)](#setFontEmbeddingMode-int) | Specifies the font embedding mode. |
| [setHeaderFooterBookmarksExportMode(int value)](#setHeaderFooterBookmarksExportMode-int) | Determines how bookmarks in headers/footers are exported. |
| [setImageColorSpaceExportMode(int value)](#setImageColorSpaceExportMode-int) | Specifies how the color space will be selected for the images in PDF document. |
| [setImageCompression(int value)](#setImageCompression-int) | Specifies compression type to be used for all images in the document. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int) | Sets a value determining how ink (InkML) objects are rendered. |
| [setInterpolateImages(boolean value)](#setInterpolateImages-boolean) | A flag indicating whether image interpolation shall be performed by a conforming reader. |
| [setJpegQuality(int value)](#setJpegQuality-int) | Sets a value determining the quality of the JPEG images inside PDF document. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean) | Sets value determining if memory optimization should be performed before saving the document. |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions) | Allows to specify metafile rendering options. |
| [setNumeralFormat(int value)](#setNumeralFormat-int) | Sets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. |
| [setOpenHyperlinksInNewWindow(boolean value)](#setOpenHyperlinksInNewWindow-boolean) | Sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean) | Flag indicates whether it is required to optimize output. |
| [setPageMode(int value)](#setPageMode-int) | Specifies how the PDF document should be displayed when opened in the PDF reader. |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet) | Sets the pages to render. |
| [setPreblendImages(boolean value)](#setPreblendImages-boolean) | Sets a value determining whether or not to preblend transparent images with black background color. |
| [setPreserveFormFields(boolean value)](#setPreserveFormFields-boolean) | Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean) | When  true , pretty formats output where applicable. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback) | Called during saving a document and accepts data about saving progress. |
| [setSaveFormat(int value)](#setSaveFormat-int) | Specifies the format in which the document will be saved if this save options object is used. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [setTextCompression(int value)](#setTextCompression-int) | Specifies compression type to be used for all textual content in the document. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean) | Sets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean) | Sets a value determining whether or not to use anti-aliasing for rendering. |
| [setUseBookFoldPrintingSettings(boolean value)](#setUseBookFoldPrintingSettings-boolean) | Sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int). |
| [setUseCoreFonts(boolean value)](#setUseCoreFonts-boolean) | Sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean) | Sets a value determining whether or not to use high quality (i.e. |
| [setZoomBehavior(int value)](#setZoomBehavior-int) | Sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. |
| [setZoomFactor(int value)](#setZoomFactor-int) | Sets a value determining zoom factor (in percentages) for a document. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### PdfSaveOptions() {#PdfSaveOptions}
```
public PdfSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.PDF](../../com.aspose.words/saveformat/\#PDF) format.

### createSaveOptions(int saveFormat) {#createSaveOptions-int}
```
public static SaveOptions createSaveOptions(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
[SaveOptions](../../com.aspose.words/saveoptions/)
### createSaveOptions(String fileName) {#createSaveOptions-java.lang.String}
```
public static SaveOptions createSaveOptions(String fileName)
```


Creates a save options object of a class suitable for the file extension specified in the given file name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The extension of this file name determines the class of the save options object to create. |

**Returns:**
[SaveOptions](../../com.aspose.words/saveoptions/) - An object of a class that derives from [SaveOptions](../../com.aspose.words/saveoptions/).

 **Examples:** 

Shows how to set a default template for documents that do not have attached templates.

```

 Document doc = new Document();

 // Enable automatic style updating, but do not attach a template document.
 doc.setAutomaticallyUpdateStyles(true);

 Assert.assertEquals("", doc.getAttachedTemplate());

 // Since there is no template document, the document had nowhere to track style changes.
 // Use a SaveOptions object to automatically set a template
 // if a document that we are saving does not have one.
 SaveOptions options = SaveOptions.createSaveOptions("Document.DefaultTemplate.docx");
 options.setDefaultTemplate(getMyDir() + "Business brochure.dotx");

 doc.save(getArtifactsDir() + "Document.DefaultTemplate.docx", options);
 
```
### deepClone() {#deepClone}
```
public PdfSaveOptions deepClone()
```


Creates a deep clone of this object.

**Returns:**
[PdfSaveOptions](../../com.aspose.words/pdfsaveoptions/)
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getAdditionalTextPositioning() {#getAdditionalTextPositioning}
```
public boolean getAdditionalTextPositioning()
```


A flag specifying whether to write additional text positioning operators or not.

 **Remarks:** 

If  true , additional text positioning operators are written to the output PDF. This may help to overcome issues with inaccurate text positioning with some printers. The downside is the increased PDF document size.

The default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is  false .

 **Remarks:** 

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) property is set to  true .

 **Examples:** 

Shows how to save the document with PostScript font.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("PostScriptFont");
 builder.writeln("Some text with PostScript font.");

 // Load the font with PostScript to use in the document.
 MemoryFontSource otf = new MemoryFontSource(DocumentHelper.getBytesFromStream(new FileInputStream(getFontsDir() + "AllegroOpen.otf")));
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{otf});

 // Embed TrueType fonts.
 doc.getFontInfos().setEmbedTrueTypeFonts(true);

 // Allow embedding PostScript fonts while embedding TrueType fonts.
 // Microsoft Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.
 SaveOptions saveOptions = SaveOptions.createSaveOptions(SaveFormat.DOCX);
 saveOptions.setAllowEmbeddingPostScriptFonts(true);

 doc.save(getArtifactsDir() + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
 
```

**Returns:**
boolean - A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved.
### getCacheBackgroundGraphics() {#getCacheBackgroundGraphics}
```
public boolean getCacheBackgroundGraphics()
```


Gets a value determining whether or not to cache graphics placed in document's background.

 **Remarks:** 

Default value is  true  and background graphics are written to the PDF document as an xObject.

When the value is  false  background graphics are not cached.

Some shapes are not supported for caching(shapes with fields, bookmarks, HRefs).

Document background graphic is various shapes, charts, images placed in the footer or header, well as background and border of a page.

**Returns:**
boolean - A value determining whether or not to cache graphics placed in document's background.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getColorMode() {#getColorMode}
```
public int getColorMode()
```


Gets a value determining how colors are rendered.

 **Remarks:** 

The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode/\#NORMAL).

**Returns:**
int - A value determining how colors are rendered. The returned value is one of [ColorMode](../../com.aspose.words/colormode/) constants.
### getCompliance() {#getCompliance}
```
public int getCompliance()
```


Specifies the PDF standards compliance level for output documents.

 **Remarks:** 

Default is [PdfCompliance.PDF\_17](../../com.aspose.words/pdfcompliance/\#PDF-17).

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfCompliance](../../com.aspose.words/pdfcompliance/) constants.
### getCreateNoteHyperlinks() {#getCreateNoteHyperlinks}
```
public boolean getCreateNoteHyperlinks()
```


Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getCustomPropertiesExport() {#getCustomPropertiesExport}
```
public int getCustomPropertiesExport()
```


Gets a value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) are exported to PDF file.

 **Remarks:** 

Default value is [PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport/\#NONE).

[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport/\#METADATA) value is not supported when saving to PDF/A. [PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport/\#STANDARD) will be used instead for PDF/A-1 and PDF/A-2 and [PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport/\#NONE) for PDF/A-4.

[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport/\#STANDARD) value is not supported when saving to PDF 2.0. [PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport/\#METADATA) will be used instead.

**Returns:**
int - A value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) are exported to PDF file. The returned value is one of [PdfCustomPropertiesExport](../../com.aspose.words/pdfcustompropertiesexport/) constants.
### getDefaultTemplate() {#getDefaultTemplate}
```
public String getDefaultTemplate()
```


Gets path to default template (including filename). Default value for this property is **empty string**.

 **Remarks:** 

If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document/\#getAutomaticallyUpdateStyles) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document/\#setAutomaticallyUpdateStyles-boolean) is  true , but [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) is empty.

 **Examples:** 

Shows how to set a default template for documents that do not have attached templates.

```

 Document doc = new Document();

 // Enable automatic style updating, but do not attach a template document.
 doc.setAutomaticallyUpdateStyles(true);

 Assert.assertEquals("", doc.getAttachedTemplate());

 // Since there is no template document, the document had nowhere to track style changes.
 // Use a SaveOptions object to automatically set a template
 // if a document that we are saving does not have one.
 SaveOptions options = SaveOptions.createSaveOptions("Document.DefaultTemplate.docx");
 options.setDefaultTemplate(getMyDir() + "Business brochure.dotx");

 doc.save(getArtifactsDir() + "Document.DefaultTemplate.docx", options);
 
```

**Returns:**
java.lang.String - Path to default template (including filename).
### getDigitalSignatureDetails() {#getDigitalSignatureDetails}
```
public PdfDigitalSignatureDetails getDigitalSignatureDetails()
```


Gets the details for signing the output PDF document.

 **Remarks:** 

The default value is  null  and the output document will not be signed. When this property is set to a valid [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails/) object, then the output PDF document will be digitally signed.

**Returns:**
[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails/) - The details for signing the output PDF document.
### getDisplayDocTitle() {#getDisplayDocTitle}
```
public boolean getDisplayDocTitle()
```


A flag specifying whether the window\\u2019s title bar should display the document title taken from the Title entry of the document information dictionary.

 **Remarks:** 

If  false , the title bar should instead display the name of the PDF file containing the document.

This flag is required by PDF/UA compliance.  true  value will be used automatically when saving to PDF/UA.

The default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getDml3DEffectsRenderingMode() {#getDml3DEffectsRenderingMode}
```
public int getDml3DEffectsRenderingMode()
```


Gets a value determining how 3D effects are rendered.

 **Remarks:** 

The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC).

**Returns:**
int - A value determining how 3D effects are rendered. The returned value is one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode/) constants.
### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode}
```
public int getDmlEffectsRenderingMode()
```


Gets a value determining how DrawingML effects are rendered.

 **Remarks:** 

The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

If [getCompliance()](../../com.aspose.words/pdfsaveoptions/\#getCompliance) / [setCompliance(int)](../../com.aspose.words/pdfsaveoptions/\#setCompliance-int) is set to [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A) or [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B), property always returns [DmlEffectsRenderingMode.NONE](../../com.aspose.words/dmleffectsrenderingmode/\#NONE).

**Returns:**
int - A value determining how DrawingML effects are rendered. The returned value is one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode/) constants.
### getDmlRenderingMode() {#getDmlRenderingMode}
```
public int getDmlRenderingMode()
```


Gets a value determining how DrawingML shapes are rendered.

 **Remarks:** 

The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode/\#FALLBACK).

This property is used when the document is exported to fixed page formats.

**Returns:**
int - A value determining how DrawingML shapes are rendered. The returned value is one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) constants.
### getDownsampleOptions() {#getDownsampleOptions}
```
public DownsampleOptions getDownsampleOptions()
```


Allows to specify downsample options.

**Returns:**
[DownsampleOptions](../../com.aspose.words/downsampleoptions/) - The corresponding [DownsampleOptions](../../com.aspose.words/downsampleoptions/) value.
### getEmbedAttachments() {#getEmbedAttachments}
```
public boolean getEmbedAttachments()
```


Gets a value determining whether or not to embed attachments to the PDF document.

 **Remarks:** 

Default value is  false  and attachments are not embedded.

When the value is  true  attachments are embedded to the PDF document.

Embedding attachments is not supported when saving to PDF/A and PDF/UA compliance.  false  value will be used automatically.

Embedding attachments is not supported when encryption is enabled.  false  value will be used automatically.

**Returns:**
boolean - A value determining whether or not to embed attachments to the PDF document.
### getEmbedFullFonts() {#getEmbedFullFonts}
```
public boolean getEmbedFullFonts()
```


Controls how fonts are embedded into the resulting PDF documents.

 **Remarks:** 

The default value is  false , which means the fonts are subsetted before embedding. Subsetting is useful if you want to keep the output file size smaller. Subsetting removes all unused glyphs from a font.

When this value is set to  true , a complete font file is embedded into PDF without subsetting. This will result in larger output files, but can be a useful option when you want to edit the resulting PDF later (e.g. add more text).

Some fonts are large (several megabytes) and embedding them without subsetting will result in large output documents.

**Returns:**
boolean - The corresponding  boolean  value.
### getEncryptionDetails() {#getEncryptionDetails}
```
public PdfEncryptionDetails getEncryptionDetails()
```


Gets the details for encrypting the output PDF document.

 **Remarks:** 

The default value is  null  and the output document will not be encrypted. When this property is set to a valid [PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails/) object, then the output PDF document will be encrypted.

AES-128 encryption algorithm is used when saving to PDF 1.7 based compliance (including PDF/UA-1). AES-256 encryption algorithm is used when saving to PDF 2.0 based compliance.

Encryption is prohibited by PDF/A compliance. This option will be ignored when saving to PDF/A.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0.

**Returns:**
[PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails/) - The details for encrypting the output PDF document.
### getExportDocumentStructure() {#getExportDocumentStructure}
```
public boolean getExportDocumentStructure()
```


Gets a value determining whether or not to export document structure.

 **Remarks:** 

This value is ignored when saving to PDF/A-1a, PDF/A-2a and PDF/UA-1 because document structure is required for this compliance.

Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

**Returns:**
boolean - A value determining whether or not to export document structure.
### getExportGeneratorName() {#getExportGeneratorName}
```
public boolean getExportGeneratorName()
```


When  true , causes the name and version of Aspose.Words to be embedded into produced files. Default value is  true .

 **Examples:** 

Shows how to disable adding name and version of Aspose.Words into produced files.

```

 Document doc = new Document();

 // Use https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ to know how to check the result.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setExportGeneratorName(false); }

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getExportLanguageToSpanTag() {#getExportLanguageToSpanTag}
```
public boolean getExportLanguageToSpanTag()
```


Gets a value determining whether or not to create a "Span" tag in the document structure to export the text language.

 **Remarks:** 

Default value is  false  and "Lang" attribute is attached to a marked-content sequence in a page content stream.

When the value is  true  "Span" tag is created for the text with non-default language and "Lang" attribute is attached to this tag.

This value is ignored when [getExportDocumentStructure()](../../com.aspose.words/pdfsaveoptions/\#getExportDocumentStructure) / [setExportDocumentStructure(boolean)](../../com.aspose.words/pdfsaveoptions/\#setExportDocumentStructure-boolean) is  false .

**Returns:**
boolean - A value determining whether or not to create a "Span" tag in the document structure to export the text language.
### getFontEmbeddingMode() {#getFontEmbeddingMode}
```
public int getFontEmbeddingMode()
```


Specifies the font embedding mode.

 **Remarks:** 

The default value is [PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode/\#EMBED-ALL).

This setting works only for the text in ANSI (Windows-1252) encoding. If the document contains non-ANSI text then corresponding fonts will be embedded regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded. [PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode/\#EMBED-ALL) value will be used automatically when saving to PDF/A and PDF/UA.

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfFontEmbeddingMode](../../com.aspose.words/pdffontembeddingmode/) constants.
### getHeaderFooterBookmarksExportMode() {#getHeaderFooterBookmarksExportMode}
```
public int getHeaderFooterBookmarksExportMode()
```


Determines how bookmarks in headers/footers are exported.

 **Remarks:** 

The default value is [HeaderFooterBookmarksExportMode.ALL](../../com.aspose.words/headerfooterbookmarksexportmode/\#ALL).

This property is used in conjunction with the [getOutlineOptions()](../../com.aspose.words/pdfsaveoptions/\#getOutlineOptions) option.

**Returns:**
int - The corresponding  int  value. The returned value is one of [HeaderFooterBookmarksExportMode](../../com.aspose.words/headerfooterbookmarksexportmode/) constants.
### getImageColorSpaceExportMode() {#getImageColorSpaceExportMode}
```
public int getImageColorSpaceExportMode()
```


Specifies how the color space will be selected for the images in PDF document.

 **Remarks:** 

The default value is [PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode/\#AUTO).

If [PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode/\#SIMPLE-CMYK) value is specified, [getImageCompression()](../../com.aspose.words/pdfsaveoptions/\#getImageCompression) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions/\#setImageCompression-int) option is ignored and Flate compression is used for all images in the document.

[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode/\#SIMPLE-CMYK) value is not supported when saving to PDF/A. [PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode/\#AUTO) value will be used instead.

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfImageColorSpaceExportMode](../../com.aspose.words/pdfimagecolorspaceexportmode/) constants.
### getImageCompression() {#getImageCompression}
```
public int getImageCompression()
```


Specifies compression type to be used for all images in the document.

 **Remarks:** 

Default is [PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression/\#AUTO).

Using [PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression/\#JPEG) lets you control the quality of images in the output document through the [getJpegQuality()](../../com.aspose.words/pdfsaveoptions/\#getJpegQuality) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions/\#setJpegQuality-int) property.

Using [PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression/\#JPEG) provides the fastest conversion speed when compared to the performance of other compression types, but in this case, there is lossy JPEG compression.

Using [PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression/\#AUTO) lets to control the quality of Jpeg in the output document through the [getJpegQuality()](../../com.aspose.words/pdfsaveoptions/\#getJpegQuality) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions/\#setJpegQuality-int) property, but for other formats, raw pixel data is extracted and saved with Flate compression. This case is slower than Jpeg conversion but lossless.

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfImageCompression](../../com.aspose.words/pdfimagecompression/) constants.
### getImlRenderingMode() {#getImlRenderingMode}
```
public int getImlRenderingMode()
```


Gets a value determining how ink (InkML) objects are rendered.

 **Remarks:** 

The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to render Ink object.

```

 Document doc = new Document(getMyDir() + "Ink object.docx");

 // Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
 // If the rendering result is unsatisfactory,
 // please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 {
     saveOptions.setImlRenderingMode(ImlRenderingMode.INK_ML);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
 
```

**Returns:**
int - A value determining how ink (InkML) objects are rendered. The returned value is one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) constants.
### getInterpolateImages() {#getInterpolateImages}
```
public boolean getInterpolateImages()
```


A flag indicating whether image interpolation shall be performed by a conforming reader. When  false  is specified, the flag is not written to the output document and the default behaviour of reader is used instead.

 **Remarks:** 

When the resolution of a source image is significantly lower than that of the output device, each source sample covers many device pixels. As a result, images can appear jaggy or blocky. These visual artifacts can be reduced by applying an image interpolation algorithm during rendering. Instead of painting all pixels covered by a source sample with the same color, image interpolation attempts to produce a smooth transition between adjacent sample values.

A conforming Reader may choose to not implement this feature of PDF, or may use any specific implementation of interpolation that it wishes.

The default value is  false .

Interpolation flag is prohibited by PDF/A compliance.  false  value will be used automatically when saving to PDF/A.

**Returns:**
boolean - The corresponding  boolean  value.
### getJpegQuality() {#getJpegQuality}
```
public int getJpegQuality()
```


Gets a value determining the quality of the JPEG images inside PDF document.

 **Remarks:** 

The default value is 100.

This property is used in conjunction with the [getImageCompression()](../../com.aspose.words/pdfsaveoptions/\#getImageCompression) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions/\#setImageCompression-int) option.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in PDF format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression. If quality is 100 and source image is JPEG, it means no compression - original bytes will be saved.

**Returns:**
int - A value determining the quality of the JPEG images inside PDF document.
### getMemoryOptimization() {#getMemoryOptimization}
```
public boolean getMemoryOptimization()
```


Gets value determining if memory optimization should be performed before saving the document. Default value for this property is  false .

 **Remarks:** 

Setting this option to  true  can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

**Returns:**
boolean - Value determining if memory optimization should be performed before saving the document.
### getMetafileRenderingOptions() {#getMetafileRenderingOptions}
```
public MetafileRenderingOptions getMetafileRenderingOptions()
```


Allows to specify metafile rendering options.

**Returns:**
[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) - The corresponding [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) value.
### getNumeralFormat() {#getNumeralFormat}
```
public int getNumeralFormat()
```


Gets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. European numerals are used by default.

 **Remarks:** 

If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) is invoked automatically to update any changes.

**Returns:**
int - [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. The returned value is one of [NumeralFormat](../../com.aspose.words/numeralformat/) constants.
### getOpenHyperlinksInNewWindow() {#getOpenHyperlinksInNewWindow}
```
public boolean getOpenHyperlinksInNewWindow()
```


Gets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser.

 **Remarks:** 

The default value is  false . When this value is set to  true  hyperlinks are saved using JavaScript code. JavaScript code is  app.launchURL("URL", true); , where  URL  is a hyperlink.

Note that if this option is set to  true  hyperlinks can't work in some PDF readers e.g. Chrome, Firefox.

JavaScript actions are prohibited by PDF/A-1 and PDF/A-2 compliance.  false  will be used automatically when saving to PDF/A-1 and PDF/A-2.

**Returns:**
boolean - A value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser.
### getOptimizeOutput() {#getOptimizeOutput}
```
public boolean getOptimizeOutput()
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  false .

 **Examples:** 

Shows how to simplify a document when saving it to HTML by removing various redundant objects.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setOptimizeOutput(optimizeOutput);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

 // The size of the optimized version of the document is almost a third of the size of the unoptimized document.
 if (optimizeOutput)
     Assert.assertEquals(62521.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 else
     Assert.assertEquals(191770.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 
```

Shows how to optimize document objects while saving to xps.

```

 Document doc = new Document(getMyDir() + "Unoptimized document.docx");

 // Create an "XpsSaveOptions" object to pass to the document's "Save" method
 // to modify how that method converts the document to .XPS.
 XpsSaveOptions saveOptions = new XpsSaveOptions();

 // Set the "OptimizeOutput" property to "true" to take measures such as removing nested or empty canvases
 // and concatenating adjacent runs with identical formatting to optimize the output document's content.
 // This may affect the appearance of the document.
 // Set the "OptimizeOutput" property to "false" to save the document normally.
 saveOptions.setOptimizeOutput(optimizeOutput);

 doc.save(getArtifactsDir() + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getOutlineOptions() {#getOutlineOptions}
```
public OutlineOptions getOutlineOptions()
```


Allows to specify outline options.

 **Remarks:** 

Outlines can be created from headings and bookmarks.

For headings outline level is determined by the heading level.

It is possible to set the max heading level to be included into outlines or disable heading outlines at all.

For bookmarks outline level may be set in options as a default value for all bookmarks or as individual values for particular bookmarks.

Also, outlines can be exported to XPS format by using the same [getOutlineOptions()](../../com.aspose.words/pdfsaveoptions/\#getOutlineOptions) class.

**Returns:**
[OutlineOptions](../../com.aspose.words/outlineoptions/) - The corresponding [OutlineOptions](../../com.aspose.words/outlineoptions/) value.
### getPageMode() {#getPageMode}
```
public int getPageMode()
```


Specifies how the PDF document should be displayed when opened in the PDF reader.

 **Remarks:** 

The default value is [PdfPageMode.USE\_OUTLINES](../../com.aspose.words/pdfpagemode/\#USE-OUTLINES).

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfPageMode](../../com.aspose.words/pdfpagemode/) constants.
### getPageSavingCallback() {#getPageSavingCallback}
```
public IPageSavingCallback getPageSavingCallback()
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

 **Examples:** 

Shows how to use a callback to save a document to HTML page by page.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Returns:**
[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) - The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) value.
### getPageSet() {#getPageSet}
```
public PageSet getPageSet()
```


Gets the pages to render. Default is all the pages in the document.

 **Examples:** 

Shows how to extract pages based on exact page indices.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add five pages to the document.
 for (int i = 1; i < 6; i++) {
     builder.write("Page " + i);
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // Create an "XpsSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how that method converts the document to .XPS.
 XpsSaveOptions xpsOptions = new XpsSaveOptions();

 // Use the "PageSet" property to select a set of the document's pages to save to output XPS.
 // In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
 xpsOptions.setPageSet(new PageSet(0, 1, 3));

 doc.save(getArtifactsDir() + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
 
```

**Returns:**
[PageSet](../../com.aspose.words/pageset/) - The pages to render.
### getPreblendImages() {#getPreblendImages}
```
public boolean getPreblendImages()
```


Gets a value determining whether or not to preblend transparent images with black background color.

 **Remarks:** 

Preblending images may improve PDF document visual appearance in Adobe Reader and remove anti-aliasing artifacts.

In order to properly display preblended images, PDF viewer application must support /Matte entry in soft-mask image dictionary. Also preblending images may decrease PDF rendering performance.

The default value is  false .

**Returns:**
boolean - A value determining whether or not to preblend transparent images with black background color.
### getPreserveFormFields() {#getPreserveFormFields}
```
public boolean getPreserveFormFields()
```


Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is  false .

 **Remarks:** 

Microsoft Word form fields include text input, drop down and check box controls.

When set to  false , these fields will be exported as text to PDF. When set to  true , these fields will be exported as PDF form fields.

When exporting form fields to PDF as form fields, some formatting loss might occur because PDF form fields do not support all features of Microsoft Word form fields.

Also, the output size depends on the content size because editable forms in Microsoft Word are inline objects.

Editable forms are prohibited by PDF/A compliance.  false  value will be used automatically when saving to PDF/A.

Form fields are not supported when saving to PDF/UA.  false  value will be used automatically.

**Returns:**
boolean - The corresponding  boolean  value.
### getPrettyFormat() {#getPrettyFormat}
```
public boolean getPrettyFormat()
```


When  true , pretty formats output where applicable. Default value is  false .

 **Remarks:** 

Set to  true  to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

 **Examples:** 

Shows how to enhance the readability of the raw code of a saved .html document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.HTML);
 {
     htmlOptions.setPrettyFormat(usePrettyFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

 // Enabling pretty format makes the raw html code more readable by adding tab stop and new line characters.
 String html = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html"), StandardCharsets.UTF_8);

 if (usePrettyFormat)
     Assert.assertEquals(
             "\r\n" +
                     "\t\r\n" +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     MessageFormat.format("\t\t\r\n", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n" +
                     "\t\r\n" +
                     "\t\t \r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\tHello world!\r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\t \r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n",
             html);
 else
     Assert.assertEquals(
             "" +
                     "" +
                     MessageFormat.format("", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "" +
                     " Hello world!" +
                     "  ",
             html);
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentSavingCallback getProgressCallback()
```


Called during saving a document and accepts data about saving progress.

 **Remarks:** 

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat/\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat/\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat/\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat/\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat/\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat/\#XAML-FLOW-PACK).

 **Examples:** 

Shows how to manage a document while saving to xamlflow.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: XamlFlow, XamlFlowPack.
     XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("XamlFlowSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.XAML_FLOW,  "xamlflow"},
                     {SaveFormat.XAML_FLOW_PACK,  "xamlflowpack"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to html.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Html, Mhtml, Epub.
     HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("HtmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }

 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.HTML,  "html"},
                     {SaveFormat.MHTML,  "mhtml"},
                     {SaveFormat.EPUB,  "epub"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to docx.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Docx, FlatOpc, Docm, Dotm, Dotx.
     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("OoxmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.DOCX,  "docx"},
                     {SaveFormat.DOCM,  "docm"},
                     {SaveFormat.DOTM,  "dotm"},
                     {SaveFormat.DOTX,  "dotx"},
                     {SaveFormat.FLAT_OPC,  "flatopc"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

**Returns:**
[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) - The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) value.
### getSaveFormat() {#getSaveFormat}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.PDF](../../com.aspose.words/saveformat/\#PDF).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat/) constants.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

 **Remarks:** 

When Aspose.Words saves a document, it needs to create temporary internal structures. By default, these internal structures are created in memory and the memory usage spikes for a short period while the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

If you are saving a very large document (thousands of pages) and/or processing many documents at the same time, then the memory spike during saving can be significant enough to cause the system to throw java.lang.IndexOutOfBoundsException. Specifying a temporary folder using [getTempFolder()](../../com.aspose.words/saveoptions/\#getTempFolder) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions/\#setTempFolder-java.lang.String) will cause Aspose.Words to keep the internal structures in temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.

 **Examples:** 

Shows how to use the hard drive instead of memory when saving a document.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // When we save a document, various elements are temporarily stored in memory as the save operation is taking place.
 // We can use this option to use a temporary folder in the local file system instead,
 // which will reduce our application's memory overhead.
 DocSaveOptions options = new DocSaveOptions();
 options.setTempFolder(getArtifactsDir() + "TempFiles");

 // The specified temporary folder must exist in the local file system before the save operation.
 new File(options.getTempFolder()).mkdir();

 doc.save(getArtifactsDir() + "DocSaveOptions.TempFolder.doc", options);

 // The folder will persist with no residual contents from the load operation.
 Assert.assertEquals(new File(options.getTempFolder()).listFiles().length, 0);
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getTextCompression() {#getTextCompression}
```
public int getTextCompression()
```


Specifies compression type to be used for all textual content in the document.

 **Remarks:** 

Default is [PdfTextCompression.FLATE](../../com.aspose.words/pdftextcompression/\#FLATE).

Significantly increases output size when saving a document without compression.

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfTextCompression](../../com.aspose.words/pdftextcompression/) constants.
### getUpdateCreatedTimeProperty() {#getUpdateCreatedTimeProperty}
```
public boolean getUpdateCreatedTimeProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. Default value is  false ;

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving.
### getUpdateFields() {#getUpdateFields}
```
public boolean getUpdateFields()
```


Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is  true .

 **Remarks:** 

Allows to specify whether to mimic or not MS Word behavior.

**Returns:**
boolean - A value determining if fields of certain types should be updated before saving the document to a fixed page format.
### getUpdateLastPrintedProperty() {#getUpdateLastPrintedProperty}
```
public boolean getUpdateLastPrintedProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to update a document's "CreatedTime" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setCreatedTime(calendar.getTime());

 // This flag determines whether the created time, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the created time.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);
 
```

Shows how to update a document's "Last printed" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setLastPrinted(calendar.getTime());

 // This flag determines whether the last printed date, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the print date.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateLastPrintedProperty(isUpdateLastPrintedProperty);

 // In Microsoft Word 2003, this property can be found via File -> Properties -> Statistics -> Printed.
 // It can also be displayed in the document's body by using a PRINTDATE field.
 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);
 
```

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.
### getUpdateLastSavedTimeProperty() {#getUpdateLastSavedTimeProperty}
```
public boolean getUpdateLastSavedTimeProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to determine whether to preserve the document's "Last saved time" property when saving.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
 // and then pass it to the document's saving method to modify how we save the document.
 // Set the "UpdateLastSavedTimeProperty" property to "true" to
 // set the output document's "Last saved time" built-in property to the current date/time.
 // Set the "UpdateLastSavedTimeProperty" property to "false" to
 // preserve the original value of the input document's "Last saved time" built-in property.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setUpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);
 
```

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.
### getUpdateSdtContent() {#getUpdateSdtContent}
```
public boolean getUpdateSdtContent()
```


Gets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to update structured document tags while saving a document to PDF.

```

 Document doc = new Document();

 // Insert a drop-down list structured document tag.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 tag.getListItems().add(new SdtListItem("Value 1"));
 tag.getListItems().add(new SdtListItem("Value 2"));
 tag.getListItems().add(new SdtListItem("Value 3"));

 // The drop-down list currently displays "Choose an item" as the default text.
 // Set the "SelectedValue" property to one of the list items to get the tag to
 // display that list item's value instead of the default text.
 tag.getListItems().setSelectedValue(tag.getListItems().get(1));

 doc.getFirstSection().getBody().appendChild(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.UpdateSdtContent.pdf");
 
```

**Returns:**
boolean - Value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving.
### getUseAntiAliasing() {#getUseAntiAliasing}
```
public boolean getUseAntiAliasing()
```


Gets a value determining whether or not to use anti-aliasing for rendering.

 **Remarks:** 

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.MOBI](../../com.aspose.words/saveformat/\#MOBI) formats this option is used for raster images.

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Returns:**
boolean - A value determining whether or not to use anti-aliasing for rendering.
### getUseBookFoldPrintingSettings() {#getUseBookFoldPrintingSettings}
```
public boolean getUseBookFoldPrintingSettings()
```


Gets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int).

 **Remarks:** 

If this option is specified, [FixedPageSaveOptions.getPageSet()](../../com.aspose.words/fixedpagesaveoptions/\#getPageSet) / [FixedPageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/fixedpagesaveoptions/\#setPageSet-com.aspose.words.PageSet) is ignored when saving. This behavior matches MS Word. If book fold printing settings are not specified in page setup, this option will have no effect.

**Returns:**
boolean - A boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int).
### getUseCoreFonts() {#getUseCoreFonts}
```
public boolean getUseCoreFonts()
```


Gets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts.

 **Remarks:** 

The default value is  false . When this value is set to  true  Arial, Times New Roman, Courier New and Symbol fonts are replaced in PDF document with corresponding core Type 1 font.

Core PDF fonts, or their font metrics and suitable substitution fonts, are required to be available to any PDF viewer application.

This setting works only for the text in ANSI (Windows-1252) encoding. Non-ANSI text will be written with embedded TrueType font regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded.  false  value will be used automatically when saving to PDF/A and PDF/UA.

Core fonts are not supported when saving to PDF 2.0 format.  false  value will be used automatically when saving to PDF 2.0.

This option has a higher priority then [getFontEmbeddingMode()](../../com.aspose.words/pdfsaveoptions/\#getFontEmbeddingMode) / [setFontEmbeddingMode(int)](../../com.aspose.words/pdfsaveoptions/\#setFontEmbeddingMode-int) option.

**Returns:**
boolean - A value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts.
### getUseHighQualityRendering() {#getUseHighQualityRendering}
```
public boolean getUseHighQualityRendering()
```


Gets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.

 **Remarks:** 

The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF).

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Returns:**
boolean - A value determining whether or not to use high quality (i.e.
### getZoomBehavior() {#getZoomBehavior}
```
public int getZoomBehavior()
```


Gets a value determining what type of zoom should be applied when a document is opened with a PDF viewer.

 **Remarks:** 

The default value is [PdfZoomBehavior.NONE](../../com.aspose.words/pdfzoombehavior/\#NONE), i.e. no fit is applied.

**Returns:**
int - A value determining what type of zoom should be applied when a document is opened with a PDF viewer. The returned value is one of [PdfZoomBehavior](../../com.aspose.words/pdfzoombehavior/) constants.
### getZoomFactor() {#getZoomFactor}
```
public int getZoomFactor()
```


Gets a value determining zoom factor (in percentages) for a document.

 **Remarks:** 

This value is used only if [getZoomBehavior()](../../com.aspose.words/pdfsaveoptions/\#getZoomBehavior) / [setZoomBehavior(int)](../../com.aspose.words/pdfsaveoptions/\#setZoomBehavior-int) is set to [PdfZoomBehavior.ZOOM\_FACTOR](../../com.aspose.words/pdfzoombehavior/\#ZOOM-FACTOR).

**Returns:**
int - A value determining zoom factor (in percentages) for a document.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setAdditionalTextPositioning(boolean value) {#setAdditionalTextPositioning-boolean}
```
public void setAdditionalTextPositioning(boolean value)
```


A flag specifying whether to write additional text positioning operators or not.

 **Remarks:** 

If  true , additional text positioning operators are written to the output PDF. This may help to overcome issues with inaccurate text positioning with some printers. The downside is the increased PDF document size.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setAllowEmbeddingPostScriptFonts(boolean value) {#setAllowEmbeddingPostScriptFonts-boolean}
```
public void setAllowEmbeddingPostScriptFonts(boolean value)
```


Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is  false .

 **Remarks:** 

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) property is set to  true .

 **Examples:** 

Shows how to save the document with PostScript font.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("PostScriptFont");
 builder.writeln("Some text with PostScript font.");

 // Load the font with PostScript to use in the document.
 MemoryFontSource otf = new MemoryFontSource(DocumentHelper.getBytesFromStream(new FileInputStream(getFontsDir() + "AllegroOpen.otf")));
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().setFontsSources(new FontSourceBase[]{otf});

 // Embed TrueType fonts.
 doc.getFontInfos().setEmbedTrueTypeFonts(true);

 // Allow embedding PostScript fonts while embedding TrueType fonts.
 // Microsoft Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.
 SaveOptions saveOptions = SaveOptions.createSaveOptions(SaveFormat.DOCX);
 saveOptions.setAllowEmbeddingPostScriptFonts(true);

 doc.save(getArtifactsDir() + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |

### setCacheBackgroundGraphics(boolean value) {#setCacheBackgroundGraphics-boolean}
```
public void setCacheBackgroundGraphics(boolean value)
```


Sets a value determining whether or not to cache graphics placed in document's background.

 **Remarks:** 

Default value is  true  and background graphics are written to the PDF document as an xObject.

When the value is  false  background graphics are not cached.

Some shapes are not supported for caching(shapes with fields, bookmarks, HRefs).

Document background graphic is various shapes, charts, images placed in the footer or header, well as background and border of a page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to cache graphics placed in document's background. |

### setColorMode(int value) {#setColorMode-int}
```
public void setColorMode(int value)
```


Sets a value determining how colors are rendered.

 **Remarks:** 

The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode/\#NORMAL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how colors are rendered. The value must be one of [ColorMode](../../com.aspose.words/colormode/) constants. |

### setCompliance(int value) {#setCompliance-int}
```
public void setCompliance(int value)
```


Specifies the PDF standards compliance level for output documents.

 **Remarks:** 

Default is [PdfCompliance.PDF\_17](../../com.aspose.words/pdfcompliance/\#PDF-17).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfCompliance](../../com.aspose.words/pdfcompliance/) constants. |

### setCreateNoteHyperlinks(boolean value) {#setCreateNoteHyperlinks-boolean}
```
public void setCreateNoteHyperlinks(boolean value)
```


Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setCustomPropertiesExport(int value) {#setCustomPropertiesExport-int}
```
public void setCustomPropertiesExport(int value)
```


Sets a value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) are exported to PDF file.

 **Remarks:** 

Default value is [PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport/\#NONE).

[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport/\#METADATA) value is not supported when saving to PDF/A. [PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport/\#STANDARD) will be used instead for PDF/A-1 and PDF/A-2 and [PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport/\#NONE) for PDF/A-4.

[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport/\#STANDARD) value is not supported when saving to PDF 2.0. [PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport/\#METADATA) will be used instead.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) are exported to PDF file. The value must be one of [PdfCustomPropertiesExport](../../com.aspose.words/pdfcustompropertiesexport/) constants. |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String}
```
public void setDefaultTemplate(String value)
```


Sets path to default template (including filename). Default value for this property is **empty string**.

 **Remarks:** 

If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document/\#getAutomaticallyUpdateStyles) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document/\#setAutomaticallyUpdateStyles-boolean) is  true , but [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) is empty.

 **Examples:** 

Shows how to set a default template for documents that do not have attached templates.

```

 Document doc = new Document();

 // Enable automatic style updating, but do not attach a template document.
 doc.setAutomaticallyUpdateStyles(true);

 Assert.assertEquals("", doc.getAttachedTemplate());

 // Since there is no template document, the document had nowhere to track style changes.
 // Use a SaveOptions object to automatically set a template
 // if a document that we are saving does not have one.
 SaveOptions options = SaveOptions.createSaveOptions("Document.DefaultTemplate.docx");
 options.setDefaultTemplate(getMyDir() + "Business brochure.dotx");

 doc.save(getArtifactsDir() + "Document.DefaultTemplate.docx", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Path to default template (including filename). |

### setDigitalSignatureDetails(PdfDigitalSignatureDetails value) {#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails}
```
public void setDigitalSignatureDetails(PdfDigitalSignatureDetails value)
```


Sets the details for signing the output PDF document.

 **Remarks:** 

The default value is  null  and the output document will not be signed. When this property is set to a valid [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails/) object, then the output PDF document will be digitally signed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails/) | The details for signing the output PDF document. |

### setDisplayDocTitle(boolean value) {#setDisplayDocTitle-boolean}
```
public void setDisplayDocTitle(boolean value)
```


A flag specifying whether the window\\u2019s title bar should display the document title taken from the Title entry of the document information dictionary.

 **Remarks:** 

If  false , the title bar should instead display the name of the PDF file containing the document.

This flag is required by PDF/UA compliance.  true  value will be used automatically when saving to PDF/UA.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setDml3DEffectsRenderingMode(int value) {#setDml3DEffectsRenderingMode-int}
```
public void setDml3DEffectsRenderingMode(int value)
```


Sets a value determining how 3D effects are rendered.

 **Remarks:** 

The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how 3D effects are rendered. The value must be one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode/) constants. |

### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int}
```
public void setDmlEffectsRenderingMode(int value)
```


Sets a value determining how DrawingML effects are rendered.

 **Remarks:** 

The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

If [getCompliance()](../../com.aspose.words/pdfsaveoptions/\#getCompliance) / [setCompliance(int)](../../com.aspose.words/pdfsaveoptions/\#setCompliance-int) is set to [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A) or [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B), property always returns [DmlEffectsRenderingMode.NONE](../../com.aspose.words/dmleffectsrenderingmode/\#NONE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML effects are rendered. The value must be one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode/) constants. |

### setDmlRenderingMode(int value) {#setDmlRenderingMode-int}
```
public void setDmlRenderingMode(int value)
```


Sets a value determining how DrawingML shapes are rendered.

 **Remarks:** 

The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode/\#FALLBACK).

This property is used when the document is exported to fixed page formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML shapes are rendered. The value must be one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) constants. |

### setDownsampleOptions(DownsampleOptions value) {#setDownsampleOptions-com.aspose.words.DownsampleOptions}
```
public void setDownsampleOptions(DownsampleOptions value)
```


Allows to specify downsample options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [DownsampleOptions](../../com.aspose.words/downsampleoptions/) | The corresponding [DownsampleOptions](../../com.aspose.words/downsampleoptions/) value. |

### setEmbedAttachments(boolean value) {#setEmbedAttachments-boolean}
```
public void setEmbedAttachments(boolean value)
```


Sets a value determining whether or not to embed attachments to the PDF document.

 **Remarks:** 

Default value is  false  and attachments are not embedded.

When the value is  true  attachments are embedded to the PDF document.

Embedding attachments is not supported when saving to PDF/A and PDF/UA compliance.  false  value will be used automatically.

Embedding attachments is not supported when encryption is enabled.  false  value will be used automatically.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to embed attachments to the PDF document. |

### setEmbedFullFonts(boolean value) {#setEmbedFullFonts-boolean}
```
public void setEmbedFullFonts(boolean value)
```


Controls how fonts are embedded into the resulting PDF documents.

 **Remarks:** 

The default value is  false , which means the fonts are subsetted before embedding. Subsetting is useful if you want to keep the output file size smaller. Subsetting removes all unused glyphs from a font.

When this value is set to  true , a complete font file is embedded into PDF without subsetting. This will result in larger output files, but can be a useful option when you want to edit the resulting PDF later (e.g. add more text).

Some fonts are large (several megabytes) and embedding them without subsetting will result in large output documents.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setEncryptionDetails(PdfEncryptionDetails value) {#setEncryptionDetails-com.aspose.words.PdfEncryptionDetails}
```
public void setEncryptionDetails(PdfEncryptionDetails value)
```


Sets the details for encrypting the output PDF document.

 **Remarks:** 

The default value is  null  and the output document will not be encrypted. When this property is set to a valid [PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails/) object, then the output PDF document will be encrypted.

AES-128 encryption algorithm is used when saving to PDF 1.7 based compliance (including PDF/UA-1). AES-256 encryption algorithm is used when saving to PDF 2.0 based compliance.

Encryption is prohibited by PDF/A compliance. This option will be ignored when saving to PDF/A.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions/\#CONTENT-COPY-FOR-ACCESSIBILITY) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails/) | The details for encrypting the output PDF document. |

### setExportDocumentStructure(boolean value) {#setExportDocumentStructure-boolean}
```
public void setExportDocumentStructure(boolean value)
```


Sets a value determining whether or not to export document structure.

 **Remarks:** 

This value is ignored when saving to PDF/A-1a, PDF/A-2a and PDF/UA-1 because document structure is required for this compliance.

Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to export document structure. |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean}
```
public void setExportGeneratorName(boolean value)
```


When  true , causes the name and version of Aspose.Words to be embedded into produced files. Default value is  true .

 **Examples:** 

Shows how to disable adding name and version of Aspose.Words into produced files.

```

 Document doc = new Document();

 // Use https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ to know how to check the result.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setExportGeneratorName(false); }

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportLanguageToSpanTag(boolean value) {#setExportLanguageToSpanTag-boolean}
```
public void setExportLanguageToSpanTag(boolean value)
```


Sets a value determining whether or not to create a "Span" tag in the document structure to export the text language.

 **Remarks:** 

Default value is  false  and "Lang" attribute is attached to a marked-content sequence in a page content stream.

When the value is  true  "Span" tag is created for the text with non-default language and "Lang" attribute is attached to this tag.

This value is ignored when [getExportDocumentStructure()](../../com.aspose.words/pdfsaveoptions/\#getExportDocumentStructure) / [setExportDocumentStructure(boolean)](../../com.aspose.words/pdfsaveoptions/\#setExportDocumentStructure-boolean) is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to create a "Span" tag in the document structure to export the text language. |

### setFontEmbeddingMode(int value) {#setFontEmbeddingMode-int}
```
public void setFontEmbeddingMode(int value)
```


Specifies the font embedding mode.

 **Remarks:** 

The default value is [PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode/\#EMBED-ALL).

This setting works only for the text in ANSI (Windows-1252) encoding. If the document contains non-ANSI text then corresponding fonts will be embedded regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded. [PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode/\#EMBED-ALL) value will be used automatically when saving to PDF/A and PDF/UA.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfFontEmbeddingMode](../../com.aspose.words/pdffontembeddingmode/) constants. |

### setHeaderFooterBookmarksExportMode(int value) {#setHeaderFooterBookmarksExportMode-int}
```
public void setHeaderFooterBookmarksExportMode(int value)
```


Determines how bookmarks in headers/footers are exported.

 **Remarks:** 

The default value is [HeaderFooterBookmarksExportMode.ALL](../../com.aspose.words/headerfooterbookmarksexportmode/\#ALL).

This property is used in conjunction with the [getOutlineOptions()](../../com.aspose.words/pdfsaveoptions/\#getOutlineOptions) option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HeaderFooterBookmarksExportMode](../../com.aspose.words/headerfooterbookmarksexportmode/) constants. |

### setImageColorSpaceExportMode(int value) {#setImageColorSpaceExportMode-int}
```
public void setImageColorSpaceExportMode(int value)
```


Specifies how the color space will be selected for the images in PDF document.

 **Remarks:** 

The default value is [PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode/\#AUTO).

If [PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode/\#SIMPLE-CMYK) value is specified, [getImageCompression()](../../com.aspose.words/pdfsaveoptions/\#getImageCompression) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions/\#setImageCompression-int) option is ignored and Flate compression is used for all images in the document.

[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode/\#SIMPLE-CMYK) value is not supported when saving to PDF/A. [PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode/\#AUTO) value will be used instead.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfImageColorSpaceExportMode](../../com.aspose.words/pdfimagecolorspaceexportmode/) constants. |

### setImageCompression(int value) {#setImageCompression-int}
```
public void setImageCompression(int value)
```


Specifies compression type to be used for all images in the document.

 **Remarks:** 

Default is [PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression/\#AUTO).

Using [PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression/\#JPEG) lets you control the quality of images in the output document through the [getJpegQuality()](../../com.aspose.words/pdfsaveoptions/\#getJpegQuality) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions/\#setJpegQuality-int) property.

Using [PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression/\#JPEG) provides the fastest conversion speed when compared to the performance of other compression types, but in this case, there is lossy JPEG compression.

Using [PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression/\#AUTO) lets to control the quality of Jpeg in the output document through the [getJpegQuality()](../../com.aspose.words/pdfsaveoptions/\#getJpegQuality) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions/\#setJpegQuality-int) property, but for other formats, raw pixel data is extracted and saved with Flate compression. This case is slower than Jpeg conversion but lossless.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfImageCompression](../../com.aspose.words/pdfimagecompression/) constants. |

### setImlRenderingMode(int value) {#setImlRenderingMode-int}
```
public void setImlRenderingMode(int value)
```


Sets a value determining how ink (InkML) objects are rendered.

 **Remarks:** 

The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

This property is used when the document is exported to fixed page formats.

 **Examples:** 

Shows how to render Ink object.

```

 Document doc = new Document(getMyDir() + "Ink object.docx");

 // Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
 // If the rendering result is unsatisfactory,
 // please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 {
     saveOptions.setImlRenderingMode(ImlRenderingMode.INK_ML);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how ink (InkML) objects are rendered. The value must be one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) constants. |

### setInterpolateImages(boolean value) {#setInterpolateImages-boolean}
```
public void setInterpolateImages(boolean value)
```


A flag indicating whether image interpolation shall be performed by a conforming reader. When  false  is specified, the flag is not written to the output document and the default behaviour of reader is used instead.

 **Remarks:** 

When the resolution of a source image is significantly lower than that of the output device, each source sample covers many device pixels. As a result, images can appear jaggy or blocky. These visual artifacts can be reduced by applying an image interpolation algorithm during rendering. Instead of painting all pixels covered by a source sample with the same color, image interpolation attempts to produce a smooth transition between adjacent sample values.

A conforming Reader may choose to not implement this feature of PDF, or may use any specific implementation of interpolation that it wishes.

The default value is  false .

Interpolation flag is prohibited by PDF/A compliance.  false  value will be used automatically when saving to PDF/A.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setJpegQuality(int value) {#setJpegQuality-int}
```
public void setJpegQuality(int value)
```


Sets a value determining the quality of the JPEG images inside PDF document.

 **Remarks:** 

The default value is 100.

This property is used in conjunction with the [getImageCompression()](../../com.aspose.words/pdfsaveoptions/\#getImageCompression) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions/\#setImageCompression-int) option.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in PDF format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression. If quality is 100 and source image is JPEG, it means no compression - original bytes will be saved.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining the quality of the JPEG images inside PDF document. |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean}
```
public void setMemoryOptimization(boolean value)
```


Sets value determining if memory optimization should be performed before saving the document. Default value for this property is  false .

 **Remarks:** 

Setting this option to  true  can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining if memory optimization should be performed before saving the document. |

### setMetafileRenderingOptions(MetafileRenderingOptions value) {#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions}
```
public void setMetafileRenderingOptions(MetafileRenderingOptions value)
```


Allows to specify metafile rendering options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) | The corresponding [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions/) value. |

### setNumeralFormat(int value) {#setNumeralFormat-int}
```
public void setNumeralFormat(int value)
```


Sets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. European numerals are used by default.

 **Remarks:** 

If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) is invoked automatically to update any changes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. The value must be one of [NumeralFormat](../../com.aspose.words/numeralformat/) constants. |

### setOpenHyperlinksInNewWindow(boolean value) {#setOpenHyperlinksInNewWindow-boolean}
```
public void setOpenHyperlinksInNewWindow(boolean value)
```


Sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser.

 **Remarks:** 

The default value is  false . When this value is set to  true  hyperlinks are saved using JavaScript code. JavaScript code is  app.launchURL("URL", true); , where  URL  is a hyperlink.

Note that if this option is set to  true  hyperlinks can't work in some PDF readers e.g. Chrome, Firefox.

JavaScript actions are prohibited by PDF/A-1 and PDF/A-2 compliance.  false  will be used automatically when saving to PDF/A-1 and PDF/A-2.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |

### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean}
```
public void setOptimizeOutput(boolean value)
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  false .

 **Examples:** 

Shows how to simplify a document when saving it to HTML by removing various redundant objects.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
 {
     saveOptions.setOptimizeOutput(optimizeOutput);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

 // The size of the optimized version of the document is almost a third of the size of the unoptimized document.
 if (optimizeOutput)
     Assert.assertEquals(62521.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 else
     Assert.assertEquals(191770.0,
         new File(getArtifactsDir() + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").length(), 200.0);
 
```

Shows how to optimize document objects while saving to xps.

```

 Document doc = new Document(getMyDir() + "Unoptimized document.docx");

 // Create an "XpsSaveOptions" object to pass to the document's "Save" method
 // to modify how that method converts the document to .XPS.
 XpsSaveOptions saveOptions = new XpsSaveOptions();

 // Set the "OptimizeOutput" property to "true" to take measures such as removing nested or empty canvases
 // and concatenating adjacent runs with identical formatting to optimize the output document's content.
 // This may affect the appearance of the document.
 // Set the "OptimizeOutput" property to "false" to save the document normally.
 saveOptions.setOptimizeOutput(optimizeOutput);

 doc.save(getArtifactsDir() + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPageMode(int value) {#setPageMode-int}
```
public void setPageMode(int value)
```


Specifies how the PDF document should be displayed when opened in the PDF reader.

 **Remarks:** 

The default value is [PdfPageMode.USE\_OUTLINES](../../com.aspose.words/pdfpagemode/\#USE-OUTLINES).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfPageMode](../../com.aspose.words/pdfpagemode/) constants. |

### setPageSavingCallback(IPageSavingCallback value) {#setPageSavingCallback-com.aspose.words.IPageSavingCallback}
```
public void setPageSavingCallback(IPageSavingCallback value)
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

 **Examples:** 

Shows how to use a callback to save a document to HTML page by page.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) | The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) value. |

### setPageSet(PageSet value) {#setPageSet-com.aspose.words.PageSet}
```
public void setPageSet(PageSet value)
```


Sets the pages to render. Default is all the pages in the document.

 **Examples:** 

Shows how to extract pages based on exact page indices.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add five pages to the document.
 for (int i = 1; i < 6; i++) {
     builder.write("Page " + i);
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // Create an "XpsSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how that method converts the document to .XPS.
 XpsSaveOptions xpsOptions = new XpsSaveOptions();

 // Use the "PageSet" property to select a set of the document's pages to save to output XPS.
 // In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
 xpsOptions.setPageSet(new PageSet(0, 1, 3));

 doc.save(getArtifactsDir() + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset/) | The pages to render. |

### setPreblendImages(boolean value) {#setPreblendImages-boolean}
```
public void setPreblendImages(boolean value)
```


Sets a value determining whether or not to preblend transparent images with black background color.

 **Remarks:** 

Preblending images may improve PDF document visual appearance in Adobe Reader and remove anti-aliasing artifacts.

In order to properly display preblended images, PDF viewer application must support /Matte entry in soft-mask image dictionary. Also preblending images may decrease PDF rendering performance.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to preblend transparent images with black background color. |

### setPreserveFormFields(boolean value) {#setPreserveFormFields-boolean}
```
public void setPreserveFormFields(boolean value)
```


Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is  false .

 **Remarks:** 

Microsoft Word form fields include text input, drop down and check box controls.

When set to  false , these fields will be exported as text to PDF. When set to  true , these fields will be exported as PDF form fields.

When exporting form fields to PDF as form fields, some formatting loss might occur because PDF form fields do not support all features of Microsoft Word form fields.

Also, the output size depends on the content size because editable forms in Microsoft Word are inline objects.

Editable forms are prohibited by PDF/A compliance.  false  value will be used automatically when saving to PDF/A.

Form fields are not supported when saving to PDF/UA.  false  value will be used automatically.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPrettyFormat(boolean value) {#setPrettyFormat-boolean}
```
public void setPrettyFormat(boolean value)
```


When  true , pretty formats output where applicable. Default value is  false .

 **Remarks:** 

Set to  true  to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

 **Examples:** 

Shows how to enhance the readability of the raw code of a saved .html document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.HTML);
 {
     htmlOptions.setPrettyFormat(usePrettyFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

 // Enabling pretty format makes the raw html code more readable by adding tab stop and new line characters.
 String html = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.PrettyFormat.html"), StandardCharsets.UTF_8);

 if (usePrettyFormat)
     Assert.assertEquals(
             "\r\n" +
                     "\t\r\n" +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     MessageFormat.format("\t\t\r\n", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n" +
                     "\t\r\n" +
                     "\t\t \r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\tHello world!\r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\t \r\n" +
                     "\t\t\t\t \r\n" +
                     "\t\t\t\r\n" +
                     "\t\t\r\n" +
                     "\t\r\n",
             html);
 else
     Assert.assertEquals(
             "" +
                     "" +
                     MessageFormat.format("", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()) +
                     "" +
                     " Hello world!" +
                     "  ",
             html);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setProgressCallback(IDocumentSavingCallback value) {#setProgressCallback-com.aspose.words.IDocumentSavingCallback}
```
public void setProgressCallback(IDocumentSavingCallback value)
```


Called during saving a document and accepts data about saving progress.

 **Remarks:** 

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat/\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat/\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat/\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat/\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat/\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat/\#XAML-FLOW-PACK).

 **Examples:** 

Shows how to manage a document while saving to xamlflow.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: XamlFlow, XamlFlowPack.
     XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("XamlFlowSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.XAML_FLOW,  "xamlflow"},
                     {SaveFormat.XAML_FLOW_PACK,  "xamlflowpack"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to html.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Html, Mhtml, Epub.
     HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("HtmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }

 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.HTML,  "html"},
                     {SaveFormat.MHTML,  "mhtml"},
                     {SaveFormat.EPUB,  "epub"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

Shows how to manage a document while saving to docx.

```

 public void progressCallback(int saveFormat, String ext) throws Exception
 {
     Document doc = new Document(getMyDir() + "Big document.docx");

     // Following formats are supported: Docx, FlatOpc, Docm, Dotm, Dotx.
     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat);
     {
         saveOptions.setProgressCallback(new SavingProgressCallback());
     }

     try {
         doc.save(getArtifactsDir() + MessageFormat.format("OoxmlSaveOptions.ProgressCallback.{0}", ext), saveOptions);
     }
     catch (IllegalStateException exception) {
         Assert.assertTrue(exception.getMessage().contains("EstimatedProgress"));
     }
 }

 public static Object[][] progressCallbackDataProvider() throws Exception
 {
     return new Object[][]
             {
                     {SaveFormat.DOCX,  "docx"},
                     {SaveFormat.DOCM,  "docm"},
                     {SaveFormat.DOTM,  "dotm"},
                     {SaveFormat.DOTX,  "dotx"},
                     {SaveFormat.FLAT_OPC,  "flatopc"},
             };
 }

 /// 
 /// Saving progress callback. Cancel a document saving after the "MaxDuration" seconds.
 /// 
 public static class SavingProgressCallback implements IDocumentSavingCallback
 {
     /// 
     /// Ctr.
     /// 
     public SavingProgressCallback()
     {
         mSavingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document saving.
     /// 
     /// Saving arguments.
     public void notify(DocumentSavingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mSavingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document saving is started.
     /// 
     private Date mSavingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.01d;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) | The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) value. |

### setSaveFormat(int value) {#setSaveFormat-int}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.PDF](../../com.aspose.words/saveformat/\#PDF).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat/) constants. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

 **Remarks:** 

When Aspose.Words saves a document, it needs to create temporary internal structures. By default, these internal structures are created in memory and the memory usage spikes for a short period while the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

If you are saving a very large document (thousands of pages) and/or processing many documents at the same time, then the memory spike during saving can be significant enough to cause the system to throw java.lang.IndexOutOfBoundsException. Specifying a temporary folder using [getTempFolder()](../../com.aspose.words/saveoptions/\#getTempFolder) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions/\#setTempFolder-java.lang.String) will cause Aspose.Words to keep the internal structures in temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.

 **Examples:** 

Shows how to use the hard drive instead of memory when saving a document.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // When we save a document, various elements are temporarily stored in memory as the save operation is taking place.
 // We can use this option to use a temporary folder in the local file system instead,
 // which will reduce our application's memory overhead.
 DocSaveOptions options = new DocSaveOptions();
 options.setTempFolder(getArtifactsDir() + "TempFiles");

 // The specified temporary folder must exist in the local file system before the save operation.
 new File(options.getTempFolder()).mkdir();

 doc.save(getArtifactsDir() + "DocSaveOptions.TempFolder.doc", options);

 // The folder will persist with no residual contents from the load operation.
 Assert.assertEquals(new File(options.getTempFolder()).listFiles().length, 0);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setTextCompression(int value) {#setTextCompression-int}
```
public void setTextCompression(int value)
```


Specifies compression type to be used for all textual content in the document.

 **Remarks:** 

Default is [PdfTextCompression.FLATE](../../com.aspose.words/pdftextcompression/\#FLATE).

Significantly increases output size when saving a document without compression.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfTextCompression](../../com.aspose.words/pdftextcompression/) constants. |

### setUpdateCreatedTimeProperty(boolean value) {#setUpdateCreatedTimeProperty-boolean}
```
public void setUpdateCreatedTimeProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. Default value is  false ;

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |

### setUpdateFields(boolean value) {#setUpdateFields-boolean}
```
public void setUpdateFields(boolean value)
```


Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is  true .

 **Remarks:** 

Allows to specify whether to mimic or not MS Word behavior.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining if fields of certain types should be updated before saving the document to a fixed page format. |

### setUpdateLastPrintedProperty(boolean value) {#setUpdateLastPrintedProperty-boolean}
```
public void setUpdateLastPrintedProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to update a document's "CreatedTime" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setCreatedTime(calendar.getTime());

 // This flag determines whether the created time, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the created time.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);
 
```

Shows how to update a document's "Last printed" property when saving.

```

 Document doc = new Document();

 Calendar calendar = Calendar.getInstance();
 calendar.set(2019, 11, 20);
 doc.getBuiltInDocumentProperties().setLastPrinted(calendar.getTime());

 // This flag determines whether the last printed date, which is a built-in property, is updated.
 // If so, then the date of the document's most recent save operation
 // with this SaveOptions object passed as a parameter is used as the print date.
 DocSaveOptions saveOptions = new DocSaveOptions();
 saveOptions.setUpdateLastPrintedProperty(isUpdateLastPrintedProperty);

 // In Microsoft Word 2003, this property can be found via File -> Properties -> Statistics -> Printed.
 // It can also be displayed in the document's body by using a PRINTDATE field.
 doc.save(getArtifactsDir() + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |

### setUpdateLastSavedTimeProperty(boolean value) {#setUpdateLastSavedTimeProperty-boolean}
```
public void setUpdateLastSavedTimeProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.

 **Examples:** 

Shows how to determine whether to preserve the document's "Last saved time" property when saving.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
 // and then pass it to the document's saving method to modify how we save the document.
 // Set the "UpdateLastSavedTimeProperty" property to "true" to
 // set the output document's "Last saved time" built-in property to the current date/time.
 // Set the "UpdateLastSavedTimeProperty" property to "false" to
 // preserve the original value of the input document's "Last saved time" built-in property.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 saveOptions.setUpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |

### setUpdateSdtContent(boolean value) {#setUpdateSdtContent-boolean}
```
public void setUpdateSdtContent(boolean value)
```


Sets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving.

 **Remarks:** 

The default value is  false .

 **Examples:** 

Shows how to update structured document tags while saving a document to PDF.

```

 Document doc = new Document();

 // Insert a drop-down list structured document tag.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DROP_DOWN_LIST, MarkupLevel.BLOCK);
 tag.getListItems().add(new SdtListItem("Value 1"));
 tag.getListItems().add(new SdtListItem("Value 2"));
 tag.getListItems().add(new SdtListItem("Value 3"));

 // The drop-down list currently displays "Choose an item" as the default text.
 // Set the "SelectedValue" property to one of the list items to get the tag to
 // display that list item's value instead of the default text.
 tag.getListItems().setSelectedValue(tag.getListItems().get(1));

 doc.getFirstSection().getBody().appendChild(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.UpdateSdtContent.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving. |

### setUseAntiAliasing(boolean value) {#setUseAntiAliasing-boolean}
```
public void setUseAntiAliasing(boolean value)
```


Sets a value determining whether or not to use anti-aliasing for rendering.

 **Remarks:** 

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.MOBI](../../com.aspose.words/saveformat/\#MOBI) formats this option is used for raster images.

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use anti-aliasing for rendering. |

### setUseBookFoldPrintingSettings(boolean value) {#setUseBookFoldPrintingSettings-boolean}
```
public void setUseBookFoldPrintingSettings(boolean value)
```


Sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int).

 **Remarks:** 

If this option is specified, [FixedPageSaveOptions.getPageSet()](../../com.aspose.words/fixedpagesaveoptions/\#getPageSet) / [FixedPageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/fixedpagesaveoptions/\#setPageSet-com.aspose.words.PageSet) is ignored when saving. This behavior matches MS Word. If book fold printing settings are not specified in page setup, this option will have no effect.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int). |

### setUseCoreFonts(boolean value) {#setUseCoreFonts-boolean}
```
public void setUseCoreFonts(boolean value)
```


Sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts.

 **Remarks:** 

The default value is  false . When this value is set to  true  Arial, Times New Roman, Courier New and Symbol fonts are replaced in PDF document with corresponding core Type 1 font.

Core PDF fonts, or their font metrics and suitable substitution fonts, are required to be available to any PDF viewer application.

This setting works only for the text in ANSI (Windows-1252) encoding. Non-ANSI text will be written with embedded TrueType font regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded.  false  value will be used automatically when saving to PDF/A and PDF/UA.

Core fonts are not supported when saving to PDF 2.0 format.  false  value will be used automatically when saving to PDF 2.0.

This option has a higher priority then [getFontEmbeddingMode()](../../com.aspose.words/pdfsaveoptions/\#getFontEmbeddingMode) / [setFontEmbeddingMode(int)](../../com.aspose.words/pdfsaveoptions/\#setFontEmbeddingMode-int) option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |

### setUseHighQualityRendering(boolean value) {#setUseHighQualityRendering-boolean}
```
public void setUseHighQualityRendering(boolean value)
```


Sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.

 **Remarks:** 

The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF).

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use high quality (i.e. |

### setZoomBehavior(int value) {#setZoomBehavior-int}
```
public void setZoomBehavior(int value)
```


Sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer.

 **Remarks:** 

The default value is [PdfZoomBehavior.NONE](../../com.aspose.words/pdfzoombehavior/\#NONE), i.e. no fit is applied.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining what type of zoom should be applied when a document is opened with a PDF viewer. The value must be one of [PdfZoomBehavior](../../com.aspose.words/pdfzoombehavior/) constants. |

### setZoomFactor(int value) {#setZoomFactor-int}
```
public void setZoomFactor(int value)
```


Sets a value determining zoom factor (in percentages) for a document.

 **Remarks:** 

This value is used only if [getZoomBehavior()](../../com.aspose.words/pdfsaveoptions/\#getZoomBehavior) / [setZoomBehavior(int)](../../com.aspose.words/pdfsaveoptions/\#setZoomBehavior-int) is set to [PdfZoomBehavior.ZOOM\_FACTOR](../../com.aspose.words/pdfzoombehavior/\#ZOOM-FACTOR).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining zoom factor (in percentages) for a document. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

