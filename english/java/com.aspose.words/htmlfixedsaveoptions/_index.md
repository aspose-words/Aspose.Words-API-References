---
title: HtmlFixedSaveOptions
linktitle: HtmlFixedSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  format in Java.
type: docs
weight: 328
url: /java/com.aspose.words/htmlfixedsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions/), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/)
```
public class HtmlFixedSaveOptions extends FixedPageSaveOptions
```

Can be used to specify additional options when saving a document into the [SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat/\#HTML-FIXED) format.

To learn more, visit the [ Specify Save Options ][Specify Save Options] documentation article.


[Specify Save Options]: https://docs.aspose.com/words/java/specify-save-options/
## Methods

| Method | Description |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts) | Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [getClass()](#getClass) |  |
| [getColorMode()](#getColorMode) | Gets a value determining how colors are rendered. |
| [getCssClassNamesPrefix()](#getCssClassNamesPrefix) | Specifies prefix which is added to all class names in style.css file. |
| [getDefaultTemplate()](#getDefaultTemplate) | Gets path to default template (including filename). |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode) | Gets a value determining how 3D effects are rendered. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode) | Gets a value determining how DrawingML effects are rendered. |
| [getDmlRenderingMode()](#getDmlRenderingMode) | Gets a value determining how DrawingML shapes are rendered. |
| [getEncoding()](#getEncoding) |  |
| [getExportEmbeddedCss()](#getExportEmbeddedCss) | Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document. |
| [getExportEmbeddedFonts()](#getExportEmbeddedFonts) | Specifies whether fonts should be embedded into Html document in Base64 format. |
| [getExportEmbeddedImages()](#getExportEmbeddedImages) | Specifies whether images should be embedded into Html document in Base64 format. |
| [getExportEmbeddedSvg()](#getExportEmbeddedSvg) | Specifies whether SVG resources should be embedded into Html document. |
| [getExportFormFields()](#getExportFormFields) | Gets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |
| [getExportGeneratorName()](#getExportGeneratorName) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [getFontFormat()](#getFontFormat) | Gets [ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. |
| [getImlRenderingMode()](#getImlRenderingMode) | Gets a value determining how ink (InkML) objects are rendered. |
| [getJpegQuality()](#getJpegQuality) | Gets a value determining the quality of the JPEG images inside Html document. |
| [getMemoryOptimization()](#getMemoryOptimization) | Gets value determining if memory optimization should be performed before saving the document. |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions) | Allows to specify metafile rendering options. |
| [getNumeralFormat()](#getNumeralFormat) | Gets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. |
| [getOptimizeOutput()](#getOptimizeOutput) | Flag indicates whether it is required to optimize output. |
| [getPageHorizontalAlignment()](#getPageHorizontalAlignment) | Specifies the horizontal alignment of pages in an HTML document. |
| [getPageMargins()](#getPageMargins) | Specifies the margins around pages in an HTML document. |
| [getPageSavingCallback()](#getPageSavingCallback) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [getPageSet()](#getPageSet) | Gets the pages to render. |
| [getPrettyFormat()](#getPrettyFormat) | When  true , pretty formats output where applicable. |
| [getProgressCallback()](#getProgressCallback) | Called during saving a document and accepts data about saving progress. |
| [getResourceSavingCallback()](#getResourceSavingCallback) | Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format. |
| [getResourcesFolder()](#getResourcesFolder) | Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. |
| [getResourcesFolderAlias()](#getResourcesFolderAlias) | Specifies the name of the folder used to construct image URIs written into an Html document. |
| [getSaveFontFaceCssSeparately()](#getSaveFontFaceCssSeparately) | Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedCss) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedCss-boolean) is  false ). |
| [getSaveFormat()](#getSaveFormat) | Specifies the format in which the document will be saved if this save options object is used. |
| [getShowPageBorder()](#getShowPageBorder) | Specifies whether border around pages should be shown. |
| [getTempFolder()](#getTempFolder) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [getUpdateFields()](#getUpdateFields) | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty) | Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [getUpdateSdtContent()](#getUpdateSdtContent) | Gets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving. |
| [getUseAntiAliasing()](#getUseAntiAliasing) | Gets a value determining whether or not to use anti-aliasing for rendering. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering) | Gets a value determining whether or not to use high quality (i.e. |
| [getUseTargetMachineFonts()](#getUseTargetMachineFonts) | Flag indicates whether fonts from target machine must be used to display the document. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean) | Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |
| [setColorMode(int value)](#setColorMode-int) | Sets a value determining how colors are rendered. |
| [setCssClassNamesPrefix(String value)](#setCssClassNamesPrefix-java.lang.String) | Specifies prefix which is added to all class names in style.css file. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String) | Sets path to default template (including filename). |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int) | Sets a value determining how 3D effects are rendered. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int) | Sets a value determining how DrawingML effects are rendered. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int) | Sets a value determining how DrawingML shapes are rendered. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) |  |
| [setExportEmbeddedCss(boolean value)](#setExportEmbeddedCss-boolean) | Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document. |
| [setExportEmbeddedFonts(boolean value)](#setExportEmbeddedFonts-boolean) | Specifies whether fonts should be embedded into Html document in Base64 format. |
| [setExportEmbeddedImages(boolean value)](#setExportEmbeddedImages-boolean) | Specifies whether images should be embedded into Html document in Base64 format. |
| [setExportEmbeddedSvg(boolean value)](#setExportEmbeddedSvg-boolean) | Specifies whether SVG resources should be embedded into Html document. |
| [setExportFormFields(boolean value)](#setExportFormFields-boolean) | Sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean) | When  true , causes the name and version of Aspose.Words to be embedded into produced files. |
| [setFontFormat(int value)](#setFontFormat-int) | Sets [ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int) | Sets a value determining how ink (InkML) objects are rendered. |
| [setJpegQuality(int value)](#setJpegQuality-int) | Sets a value determining the quality of the JPEG images inside Html document. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean) | Sets value determining if memory optimization should be performed before saving the document. |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions) | Allows to specify metafile rendering options. |
| [setNumeralFormat(int value)](#setNumeralFormat-int) | Sets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean) | Flag indicates whether it is required to optimize output. |
| [setPageHorizontalAlignment(int value)](#setPageHorizontalAlignment-int) | Specifies the horizontal alignment of pages in an HTML document. |
| [setPageMargins(double value)](#setPageMargins-double) | Specifies the margins around pages in an HTML document. |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet) | Sets the pages to render. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean) | When  true , pretty formats output where applicable. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback) | Called during saving a document and accepts data about saving progress. |
| [setResourceSavingCallback(IResourceSavingCallback value)](#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback) | Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format. |
| [setResourcesFolder(String value)](#setResourcesFolder-java.lang.String) | Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. |
| [setResourcesFolderAlias(String value)](#setResourcesFolderAlias-java.lang.String) | Specifies the name of the folder used to construct image URIs written into an Html document. |
| [setSaveFontFaceCssSeparately(boolean value)](#setSaveFontFaceCssSeparately-boolean) | Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedCss) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedCss-boolean) is  false ). |
| [setSaveFormat(int value)](#setSaveFormat-int) | Specifies the format in which the document will be saved if this save options object is used. |
| [setShowPageBorder(boolean value)](#setShowPageBorder-boolean) | Specifies whether border around pages should be shown. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties/\#getCreatedTime) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setCreatedTime-java.util.Date) property is updated before saving. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean) | Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean) | Sets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean) | Sets a value determining whether or not to use anti-aliasing for rendering. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean) | Sets a value determining whether or not to use high quality (i.e. |
| [setUseTargetMachineFonts(boolean value)](#setUseTargetMachineFonts-boolean) | Flag indicates whether fonts from target machine must be used to display the document. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


Gets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is  false .

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) property is set to  true .

**Returns:**
boolean - A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved.
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


Gets a value determining how colors are rendered. The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode/\#NORMAL).

**Returns:**
int - A value determining how colors are rendered. The returned value is one of [ColorMode](../../com.aspose.words/colormode/) constants.
### getCssClassNamesPrefix() {#getCssClassNamesPrefix}
```
public String getCssClassNamesPrefix()
```


Specifies prefix which is added to all class names in style.css file. Default value is  "aw" .

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getDefaultTemplate() {#getDefaultTemplate}
```
public String getDefaultTemplate()
```


Gets path to default template (including filename). Default value for this property is **empty string**. If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document/\#getAutomaticallyUpdateStyles) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document/\#setAutomaticallyUpdateStyles-boolean) is  true , but [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) is empty.

**Returns:**
java.lang.String - Path to default template (including filename).
### getDml3DEffectsRenderingMode() {#getDml3DEffectsRenderingMode}
```
public int getDml3DEffectsRenderingMode()
```


Gets a value determining how 3D effects are rendered. The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC).

**Returns:**
int - A value determining how 3D effects are rendered. The returned value is one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode/) constants.
### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode}
```
public int getDmlEffectsRenderingMode()
```


Gets a value determining how DrawingML effects are rendered. The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

**Returns:**
int - A value determining how DrawingML effects are rendered. The returned value is one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode/) constants.
### getDmlRenderingMode() {#getDmlRenderingMode}
```
public int getDmlRenderingMode()
```


Gets a value determining how DrawingML shapes are rendered. The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode/\#FALLBACK).

This property is used when the document is exported to fixed page formats.

**Returns:**
int - A value determining how DrawingML shapes are rendered. The returned value is one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) constants.
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```




**Returns:**
java.nio.charset.Charset
### getExportEmbeddedCss() {#getExportEmbeddedCss}
```
public boolean getExportEmbeddedCss()
```


Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document.

**Returns:**
boolean - The corresponding  boolean  value.
### getExportEmbeddedFonts() {#getExportEmbeddedFonts}
```
public boolean getExportEmbeddedFonts()
```


Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

**Returns:**
boolean - The corresponding  boolean  value.
### getExportEmbeddedImages() {#getExportEmbeddedImages}
```
public boolean getExportEmbeddedImages()
```


Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

**Returns:**
boolean - The corresponding  boolean  value.
### getExportEmbeddedSvg() {#getExportEmbeddedSvg}
```
public boolean getExportEmbeddedSvg()
```


Specifies whether SVG resources should be embedded into Html document. Default value is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### getExportFormFields() {#getExportFormFields}
```
public boolean getExportFormFields()
```


Gets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics.

**Returns:**
boolean - Indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics.
### getExportGeneratorName() {#getExportGeneratorName}
```
public boolean getExportGeneratorName()
```


When  true , causes the name and version of Aspose.Words to be embedded into produced files. Default value is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### getFontFormat() {#getFontFormat}
```
public int getFontFormat()
```


Gets [ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. Default value is [ExportFontFormat.WOFF](../../com.aspose.words/exportfontformat/\#WOFF).

**Returns:**
int - \{[ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. The returned value is one of [ExportFontFormat](../../com.aspose.words/exportfontformat/) constants.
### getImlRenderingMode() {#getImlRenderingMode}
```
public int getImlRenderingMode()
```


Gets a value determining how ink (InkML) objects are rendered. The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

This property is used when the document is exported to fixed page formats.

**Returns:**
int - A value determining how ink (InkML) objects are rendered. The returned value is one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) constants.
### getJpegQuality() {#getJpegQuality}
```
public int getJpegQuality()
```


Gets a value determining the quality of the JPEG images inside Html document.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in fixed page format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

**Returns:**
int - A value determining the quality of the JPEG images inside Html document.
### getMemoryOptimization() {#getMemoryOptimization}
```
public boolean getMemoryOptimization()
```


Gets value determining if memory optimization should be performed before saving the document. Default value for this property is  false . Setting this option to  true  can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

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


Gets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. European numerals are used by default. If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) is invoked automatically to update any changes.

**Returns:**
int - \{[NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. The returned value is one of [NumeralFormat](../../com.aspose.words/numeralformat/) constants.
### getOptimizeOutput() {#getOptimizeOutput}
```
public boolean getOptimizeOutput()
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### getPageHorizontalAlignment() {#getPageHorizontalAlignment}
```
public int getPageHorizontalAlignment()
```


Specifies the horizontal alignment of pages in an HTML document. Default value is [HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#CENTER).

**Returns:**
int - The corresponding  int  value. The returned value is one of [HtmlFixedPageHorizontalAlignment](../../com.aspose.words/htmlfixedpagehorizontalalignment/) constants.
### getPageMargins() {#getPageMargins}
```
public double getPageMargins()
```


Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points.

Depends on the value of [getPageHorizontalAlignment()](../../com.aspose.words/htmlfixedsaveoptions/\#getPageHorizontalAlignment) / [setPageHorizontalAlignment(int)](../../com.aspose.words/htmlfixedsaveoptions/\#setPageHorizontalAlignment-int) property:

 *  Defines top, bottom and left page margins if the value is [HtmlFixedPageHorizontalAlignment.LEFT](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#LEFT).
 *  Defines top, bottom and right page margins if the value is [HtmlFixedPageHorizontalAlignment.RIGHT](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#RIGHT).
 *  Defines top and bottom page margins if the value is [HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#CENTER).

**Returns:**
double - The corresponding  double  value.
### getPageSavingCallback() {#getPageSavingCallback}
```
public IPageSavingCallback getPageSavingCallback()
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

**Returns:**
[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) - The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) value.
### getPageSet() {#getPageSet}
```
public PageSet getPageSet()
```


Gets the pages to render. Default is all the pages in the document.

**Returns:**
[PageSet](../../com.aspose.words/pageset/) - The pages to render.
### getPrettyFormat() {#getPrettyFormat}
```
public boolean getPrettyFormat()
```


When  true , pretty formats output where applicable. Default value is  false .

Set to  true  to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

**Returns:**
boolean - The corresponding  boolean  value.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentSavingCallback getProgressCallback()
```


Called during saving a document and accepts data about saving progress.

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat/\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat/\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat/\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat/\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat/\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat/\#XAML-FLOW-PACK).

**Returns:**
[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) - The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) value.
### getResourceSavingCallback() {#getResourceSavingCallback}
```
public IResourceSavingCallback getResourceSavingCallback()
```


Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format.

**Returns:**
[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback/) - The corresponding [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback/) value.
### getResourcesFolder() {#getResourcesFolder}
```
public String getResourcesFolder()
```


Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is  null .

Has effect only if [getExportEmbeddedImages()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedImages) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedImages-boolean) property is  false .

When you save a [Document](../../com.aspose.words/document/) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) property

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getResourcesFolderAlias() {#getResourcesFolderAlias}
```
public String getResourcesFolderAlias()
```


Specifies the name of the folder used to construct image URIs written into an Html document. Default is  null .

When you save a [Document](../../com.aspose.words/document/) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getSaveFontFaceCssSeparately() {#getSaveFontFaceCssSeparately}
```
public boolean getSaveFontFaceCssSeparately()
```


Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedCss) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedCss-boolean) is  false ). Default value is  false , all CSS rules are written into single file "styles.css". Setting this property to  true  restores the old behavior (separate files) for compatibility with legacy code.

**Returns:**
boolean - The corresponding  boolean  value.
### getSaveFormat() {#getSaveFormat}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat/\#HTML-FIXED).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat/) constants.
### getShowPageBorder() {#getShowPageBorder}
```
public boolean getShowPageBorder()
```


Specifies whether border around pages should be shown. Default is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

When Aspose.Words saves a document, it needs to create temporary internal structures. By default, these internal structures are created in memory and the memory usage spikes for a short period while the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

If you are saving a very large document (thousands of pages) and/or processing many documents at the same time, then the memory spike during saving can be significant enough to cause the system to throw java.lang.IndexOutOfBoundsException. Specifying a temporary folder using [getTempFolder()](../../com.aspose.words/saveoptions/\#getTempFolder) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions/\#setTempFolder-java.lang.String) will cause Aspose.Words to keep the internal structures in temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
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


Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is  true . Allows to specify whether to mimic or not MS Word behavior.

**Returns:**
boolean - A value determining if fields of certain types should be updated before saving the document to a fixed page format.
### getUpdateLastPrintedProperty() {#getUpdateLastPrintedProperty}
```
public boolean getUpdateLastPrintedProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.
### getUpdateLastSavedTimeProperty() {#getUpdateLastSavedTimeProperty}
```
public boolean getUpdateLastSavedTimeProperty()
```


Gets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.

**Returns:**
boolean - A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.
### getUpdateSdtContent() {#getUpdateSdtContent}
```
public boolean getUpdateSdtContent()
```


Gets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving. The default value is  false .

**Returns:**
boolean - Value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving.
### getUseAntiAliasing() {#getUseAntiAliasing}
```
public boolean getUseAntiAliasing()
```


Gets a value determining whether or not to use anti-aliasing for rendering.

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.MOBI](../../com.aspose.words/saveformat/\#MOBI) formats this option is used for raster images.

**Returns:**
boolean - A value determining whether or not to use anti-aliasing for rendering.
### getUseHighQualityRendering() {#getUseHighQualityRendering}
```
public boolean getUseHighQualityRendering()
```


Gets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF).

**Returns:**
boolean - A value determining whether or not to use high quality (i.e.
### getUseTargetMachineFonts() {#getUseTargetMachineFonts}
```
public boolean getUseTargetMachineFonts()
```


Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to  true , [getFontFormat()](../../com.aspose.words/htmlfixedsaveoptions/\#getFontFormat) / [setFontFormat(int)](../../com.aspose.words/htmlfixedsaveoptions/\#setFontFormat-int) and [getExportEmbeddedFonts()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedFonts) / [setExportEmbeddedFonts(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedFonts-boolean) properties do not have effect, also [getResourceSavingCallback()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourceSavingCallback) / [setResourceSavingCallback(com.aspose.words.IResourceSavingCallback)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback) is not fired for fonts. Default is  false .

**Returns:**
boolean - The corresponding  boolean  value.
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




### setAllowEmbeddingPostScriptFonts(boolean value) {#setAllowEmbeddingPostScriptFonts-boolean}
```
public void setAllowEmbeddingPostScriptFonts(boolean value)
```


Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is  false .

Note, Word does not embed PostScript fonts, but can open documents with embedded fonts of this type.

This option only works when [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) of the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) property is set to  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. |

### setColorMode(int value) {#setColorMode-int}
```
public void setColorMode(int value)
```


Sets a value determining how colors are rendered. The default value is [ColorMode.NORMAL](../../com.aspose.words/colormode/\#NORMAL).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how colors are rendered. The value must be one of [ColorMode](../../com.aspose.words/colormode/) constants. |

### setCssClassNamesPrefix(String value) {#setCssClassNamesPrefix-java.lang.String}
```
public void setCssClassNamesPrefix(String value)
```


Specifies prefix which is added to all class names in style.css file. Default value is  "aw" .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String}
```
public void setDefaultTemplate(String value)
```


Sets path to default template (including filename). Default value for this property is **empty string**. If specified, this path is used to load template when [Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document/\#getAutomaticallyUpdateStyles) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document/\#setAutomaticallyUpdateStyles-boolean) is  true , but [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String) is empty.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Path to default template (including filename). |

### setDml3DEffectsRenderingMode(int value) {#setDml3DEffectsRenderingMode-int}
```
public void setDml3DEffectsRenderingMode(int value)
```


Sets a value determining how 3D effects are rendered. The default value is [Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how 3D effects are rendered. The value must be one of [Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode/) constants. |

### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int}
```
public void setDmlEffectsRenderingMode(int value)
```


Sets a value determining how DrawingML effects are rendered. The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML effects are rendered. The value must be one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode/) constants. |

### setDmlRenderingMode(int value) {#setDmlRenderingMode-int}
```
public void setDmlRenderingMode(int value)
```


Sets a value determining how DrawingML shapes are rendered. The default value is [DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode/\#FALLBACK).

This property is used when the document is exported to fixed page formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML shapes are rendered. The value must be one of [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) constants. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.nio.charset.Charset |  |

### setExportEmbeddedCss(boolean value) {#setExportEmbeddedCss-boolean}
```
public void setExportEmbeddedCss(boolean value)
```


Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportEmbeddedFonts(boolean value) {#setExportEmbeddedFonts-boolean}
```
public void setExportEmbeddedFonts(boolean value)
```


Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportEmbeddedImages(boolean value) {#setExportEmbeddedImages-boolean}
```
public void setExportEmbeddedImages(boolean value)
```


Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportEmbeddedSvg(boolean value) {#setExportEmbeddedSvg-boolean}
```
public void setExportEmbeddedSvg(boolean value)
```


Specifies whether SVG resources should be embedded into Html document. Default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExportFormFields(boolean value) {#setExportFormFields-boolean}
```
public void setExportFormFields(boolean value)
```


Sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean}
```
public void setExportGeneratorName(boolean value)
```


When  true , causes the name and version of Aspose.Words to be embedded into produced files. Default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setFontFormat(int value) {#setFontFormat-int}
```
public void setFontFormat(int value)
```


Sets [ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. Default value is [ExportFontFormat.WOFF](../../com.aspose.words/exportfontformat/\#WOFF).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | \{[ExportFontFormat](../../com.aspose.words/exportfontformat/) used for font exporting. The value must be one of [ExportFontFormat](../../com.aspose.words/exportfontformat/) constants. |

### setImlRenderingMode(int value) {#setImlRenderingMode-int}
```
public void setImlRenderingMode(int value)
```


Sets a value determining how ink (InkML) objects are rendered. The default value is [ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

This property is used when the document is exported to fixed page formats.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how ink (InkML) objects are rendered. The value must be one of [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) constants. |

### setJpegQuality(int value) {#setJpegQuality-int}
```
public void setJpegQuality(int value)
```


Sets a value determining the quality of the JPEG images inside Html document.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in fixed page format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression.

The default value is 95.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining the quality of the JPEG images inside Html document. |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean}
```
public void setMemoryOptimization(boolean value)
```


Sets value determining if memory optimization should be performed before saving the document. Default value for this property is  false . Setting this option to  true  can significantly decrease memory consumption while saving large documents at the cost of slower saving time.

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


Sets [NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. European numerals are used by default. If the value of this property is changed and page layout is already built then [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) is invoked automatically to update any changes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | \{[NumeralFormat](../../com.aspose.words/numeralformat/) used for rendering of numerals. The value must be one of [NumeralFormat](../../com.aspose.words/numeralformat/) constants. |

### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean}
```
public void setOptimizeOutput(boolean value)
```


Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to  true . Default is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPageHorizontalAlignment(int value) {#setPageHorizontalAlignment-int}
```
public void setPageHorizontalAlignment(int value)
```


Specifies the horizontal alignment of pages in an HTML document. Default value is [HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#CENTER).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HtmlFixedPageHorizontalAlignment](../../com.aspose.words/htmlfixedpagehorizontalalignment/) constants. |

### setPageMargins(double value) {#setPageMargins-double}
```
public void setPageMargins(double value)
```


Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points.

Depends on the value of [getPageHorizontalAlignment()](../../com.aspose.words/htmlfixedsaveoptions/\#getPageHorizontalAlignment) / [setPageHorizontalAlignment(int)](../../com.aspose.words/htmlfixedsaveoptions/\#setPageHorizontalAlignment-int) property:

 *  Defines top, bottom and left page margins if the value is [HtmlFixedPageHorizontalAlignment.LEFT](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#LEFT).
 *  Defines top, bottom and right page margins if the value is [HtmlFixedPageHorizontalAlignment.RIGHT](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#RIGHT).
 *  Defines top and bottom page margins if the value is [HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment/\#CENTER).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setPageSavingCallback(IPageSavingCallback value) {#setPageSavingCallback-com.aspose.words.IPageSavingCallback}
```
public void setPageSavingCallback(IPageSavingCallback value)
```


Allows to control how separate pages are saved when a document is exported to fixed page format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) | The corresponding [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback/) value. |

### setPageSet(PageSet value) {#setPageSet-com.aspose.words.PageSet}
```
public void setPageSet(PageSet value)
```


Sets the pages to render. Default is all the pages in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset/) | The pages to render. |

### setPrettyFormat(boolean value) {#setPrettyFormat-boolean}
```
public void setPrettyFormat(boolean value)
```


When  true , pretty formats output where applicable. Default value is  false .

Set to  true  to make HTML, MHTML, EPUB, WordML, RTF, DOCX and ODT output human readable. Useful for testing or debugging.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setProgressCallback(IDocumentSavingCallback value) {#setProgressCallback-com.aspose.words.IDocumentSavingCallback}
```
public void setProgressCallback(IDocumentSavingCallback value)
```


Called during saving a document and accepts data about saving progress.

Progress is reported when saving to [SaveFormat.DOCX](../../com.aspose.words/saveformat/\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat/\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat/\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat/\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat/\#XAML-FLOW), or [SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat/\#XAML-FLOW-PACK).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) | The corresponding [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback/) value. |

### setResourceSavingCallback(IResourceSavingCallback value) {#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback}
```
public void setResourceSavingCallback(IResourceSavingCallback value)
```


Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback/) | The corresponding [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback/) value. |

### setResourcesFolder(String value) {#setResourcesFolder-java.lang.String}
```
public void setResourcesFolder(String value)
```


Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is  null .

Has effect only if [getExportEmbeddedImages()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedImages) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedImages-boolean) property is  false .

When you save a [Document](../../com.aspose.words/document/) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) property

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setResourcesFolderAlias(String value) {#setResourcesFolderAlias-java.lang.String}
```
public void setResourcesFolderAlias(String value)
```


Specifies the name of the folder used to construct image URIs written into an Html document. Default is  null .

When you save a [Document](../../com.aspose.words/document/) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. [getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) allows you to specify where the images will be saved and [getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) allows to specify how the image URIs will be constructed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setSaveFontFaceCssSeparately(boolean value) {#setSaveFontFaceCssSeparately-boolean}
```
public void setSaveFontFaceCssSeparately(boolean value)
```


Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedCss) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedCss-boolean) is  false ). Default value is  false , all CSS rules are written into single file "styles.css". Setting this property to  true  restores the old behavior (separate files) for compatibility with legacy code.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSaveFormat(int value) {#setSaveFormat-int}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat/\#HTML-FIXED).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat/) constants. |

### setShowPageBorder(boolean value) {#setShowPageBorder-boolean}
```
public void setShowPageBorder(boolean value)
```


Specifies whether border around pages should be shown. Default is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is  null  and no temporary files are used.

When Aspose.Words saves a document, it needs to create temporary internal structures. By default, these internal structures are created in memory and the memory usage spikes for a short period while the document is being saved. When saving is complete, the memory is freed and reclaimed by the garbage collector.

If you are saving a very large document (thousands of pages) and/or processing many documents at the same time, then the memory spike during saving can be significant enough to cause the system to throw java.lang.IndexOutOfBoundsException. Specifying a temporary folder using [getTempFolder()](../../com.aspose.words/saveoptions/\#getTempFolder) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions/\#setTempFolder-java.lang.String) will cause Aspose.Words to keep the internal structures in temporary files instead of memory. It reduces the memory usage during saving, but will decrease the save performance.

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when saving is complete.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

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


Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is  true . Allows to specify whether to mimic or not MS Word behavior.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining if fields of certain types should be updated before saving the document to a fixed page format. |

### setUpdateLastPrintedProperty(boolean value) {#setUpdateLastPrintedProperty-boolean}
```
public void setUpdateLastPrintedProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties/\#getLastPrinted) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastPrinted-java.util.Date) property is updated before saving. |

### setUpdateLastSavedTimeProperty(boolean value) {#setUpdateLastSavedTimeProperty-boolean}
```
public void setUpdateLastSavedTimeProperty(boolean value)
```


Sets a value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether the [BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties/\#getLastSavedTime) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties/\#setLastSavedTime-java.util.Date) property is updated before saving. |

### setUpdateSdtContent(boolean value) {#setUpdateSdtContent-boolean}
```
public void setUpdateSdtContent(boolean value)
```


Sets value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining whether content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) is updated before saving. |

### setUseAntiAliasing(boolean value) {#setUseAntiAliasing-boolean}
```
public void setUseAntiAliasing(boolean value)
```


Sets a value determining whether or not to use anti-aliasing for rendering.

The default value is  false . When this value is set to  true  anti-aliasing is used for rendering.

This property is used when the document is exported to the following formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF). When the document is exported to the [SaveFormat.HTML](../../com.aspose.words/saveformat/\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat/\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat/\#EPUB), [SaveFormat.AZW\_3](../../com.aspose.words/saveformat/\#AZW-3) or [SaveFormat.MOBI](../../com.aspose.words/saveformat/\#MOBI) formats this option is used for raster images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use anti-aliasing for rendering. |

### setUseHighQualityRendering(boolean value) {#setUseHighQualityRendering-boolean}
```
public void setUseHighQualityRendering(boolean value)
```


Sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. The default value is  false .

This property is used when the document is exported to image formats: [SaveFormat.TIFF](../../com.aspose.words/saveformat/\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat/\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat/\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat/\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat/\#EMF).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to use high quality (i.e. |

### setUseTargetMachineFonts(boolean value) {#setUseTargetMachineFonts-boolean}
```
public void setUseTargetMachineFonts(boolean value)
```


Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to  true , [getFontFormat()](../../com.aspose.words/htmlfixedsaveoptions/\#getFontFormat) / [setFontFormat(int)](../../com.aspose.words/htmlfixedsaveoptions/\#setFontFormat-int) and [getExportEmbeddedFonts()](../../com.aspose.words/htmlfixedsaveoptions/\#getExportEmbeddedFonts) / [setExportEmbeddedFonts(boolean)](../../com.aspose.words/htmlfixedsaveoptions/\#setExportEmbeddedFonts-boolean) properties do not have effect, also [getResourceSavingCallback()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourceSavingCallback) / [setResourceSavingCallback(com.aspose.words.IResourceSavingCallback)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback) is not fired for fonts. Default is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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

