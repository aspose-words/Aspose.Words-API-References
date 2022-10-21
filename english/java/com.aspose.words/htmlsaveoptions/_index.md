---
title: HtmlSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the    or  format.
type: docs
weight: 331
url: /java/com.aspose.words/htmlsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class HtmlSaveOptions extends SaveOptions implements Cloneable
```

Can be used to specify additional options when saving a document into the [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) format.

To learn more, visit the **Specify Save Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [HtmlSaveOptions()](#HtmlSaveOptions--) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML) format. |
| [HtmlSaveOptions(int saveFormat)](#HtmlSaveOptions-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getAllowNegativeIndent()](#getAllowNegativeIndent--) | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. |
| [setAllowNegativeIndent(boolean value)](#setAllowNegativeIndent-boolean-) | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. |
| [getCssStyleSheetFileName()](#getCssStyleSheetFileName--) | Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. |
| [setCssStyleSheetFileName(String value)](#setCssStyleSheetFileName-java.lang.String-) | Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. |
| [getCssStyleSheetType()](#getCssStyleSheetType--) | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. |
| [setCssStyleSheetType(int value)](#setCssStyleSheetType-int-) | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. |
| [getCssClassNamePrefix()](#getCssClassNamePrefix--) | Specifies a prefix which is added to all CSS class names. |
| [setCssClassNamePrefix(String value)](#setCssClassNamePrefix-java.lang.String-) | Specifies a prefix which is added to all CSS class names. |
| [getDocumentPartSavingCallback()](#getDocumentPartSavingCallback--) | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [setDocumentPartSavingCallback(IDocumentPartSavingCallback value)](#setDocumentPartSavingCallback-com.aspose.words.IDocumentPartSavingCallback-) | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [getCssSavingCallback()](#getCssSavingCallback--) | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [setCssSavingCallback(ICssSavingCallback value)](#setCssSavingCallback-com.aspose.words.ICssSavingCallback-) | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [getDocumentSplitCriteria()](#getDocumentSplitCriteria--) | Specifies how the document should be split when saving to [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) format. |
| [setDocumentSplitCriteria(int value)](#setDocumentSplitCriteria-int-) | Specifies how the document should be split when saving to [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) format. |
| [getDocumentSplitHeadingLevel()](#getDocumentSplitHeadingLevel--) | Specifies the maximum level of headings at which to split the document. |
| [setDocumentSplitHeadingLevel(int value)](#setDocumentSplitHeadingLevel-int-) | Specifies the maximum level of headings at which to split the document. |
| [getEncoding()](#getEncoding--) |  |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) |  |
| [getEpubNavigationMapLevel()](#getEpubNavigationMapLevel--) | Specifies the maximum level of headings populated to the navigation map when exporting to IDPF EPUB format. |
| [setEpubNavigationMapLevel(int value)](#setEpubNavigationMapLevel-int-) | Specifies the maximum level of headings populated to the navigation map when exporting to IDPF EPUB format. |
| [getExportDocumentProperties()](#getExportDocumentProperties--) | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. |
| [setExportDocumentProperties(boolean value)](#setExportDocumentProperties-boolean-) | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. |
| [getExportFontResources()](#getExportFontResources--) | Specifies whether font resources should be exported to HTML, MHTML or EPUB. |
| [setExportFontResources(boolean value)](#setExportFontResources-boolean-) | Specifies whether font resources should be exported to HTML, MHTML or EPUB. |
| [getExportFontsAsBase64()](#getExportFontsAsBase64--) | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. |
| [setExportFontsAsBase64(boolean value)](#setExportFontsAsBase64-boolean-) | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. |
| [getExportHeadersFootersMode()](#getExportHeadersFootersMode--) | Specifies how headers and footers are output to HTML, MHTML or EPUB. |
| [setExportHeadersFootersMode(int value)](#setExportHeadersFootersMode-int-) | Specifies how headers and footers are output to HTML, MHTML or EPUB. |
| [getExportImagesAsBase64()](#getExportImagesAsBase64--) | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. |
| [setExportImagesAsBase64(boolean value)](#setExportImagesAsBase64-boolean-) | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. |
| [getExportLanguageInformation()](#getExportLanguageInformation--) | Specifies whether language information is exported to HTML, MHTML or EPUB. |
| [setExportLanguageInformation(boolean value)](#setExportLanguageInformation-boolean-) | Specifies whether language information is exported to HTML, MHTML or EPUB. |
| [getExportListLabels()](#getExportListLabels--) | Controls how list labels are output to HTML, MHTML or EPUB. |
| [setExportListLabels(int value)](#setExportListLabels-int-) | Controls how list labels are output to HTML, MHTML or EPUB. |
| [getMetafileFormat()](#getMetafileFormat--) | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. |
| [setMetafileFormat(int value)](#setMetafileFormat-int-) | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. |
| [getExportPageSetup()](#getExportPageSetup--) | Specifies whether page setup is exported to HTML, MHTML or EPUB. |
| [setExportPageSetup(boolean value)](#setExportPageSetup-boolean-) | Specifies whether page setup is exported to HTML, MHTML or EPUB. |
| [getExportPageMargins()](#getExportPageMargins--) | Specifies whether page margins is exported to HTML, MHTML or EPUB. |
| [setExportPageMargins(boolean value)](#setExportPageMargins-boolean-) | Specifies whether page margins is exported to HTML, MHTML or EPUB. |
| [getExportRelativeFontSize()](#getExportRelativeFontSize--) | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. |
| [setExportRelativeFontSize(boolean value)](#setExportRelativeFontSize-boolean-) | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. |
| [getExportTextInputFormFieldAsText()](#getExportTextInputFormFieldAsText--) | Controls how text input form fields are saved to HTML or MHTML. |
| [setExportTextInputFormFieldAsText(boolean value)](#setExportTextInputFormFieldAsText-boolean-) | Controls how text input form fields are saved to HTML or MHTML. |
| [getExportShapesAsSvg()](#getExportShapesAsSvg--) | Controls whether [Shape](../../com.aspose.words/shape) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. |
| [setExportShapesAsSvg(boolean value)](#setExportShapesAsSvg-boolean-) | Controls whether [Shape](../../com.aspose.words/shape) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. |
| [getExportDropDownFormFieldAsText()](#getExportDropDownFormFieldAsText--) | Controls how drop-down form fields are saved to HTML or MHTML. |
| [setExportDropDownFormFieldAsText(boolean value)](#setExportDropDownFormFieldAsText-boolean-) | Controls how drop-down form fields are saved to HTML or MHTML. |
| [getExportTocPageNumbers()](#getExportTocPageNumbers--) | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. |
| [setExportTocPageNumbers(boolean value)](#setExportTocPageNumbers-boolean-) | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. |
| [getExportXhtmlTransitional()](#getExportXhtmlTransitional--) | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. |
| [setExportXhtmlTransitional(boolean value)](#setExportXhtmlTransitional-boolean-) | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. |
| [getHtmlVersion()](#getHtmlVersion--) | Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. |
| [setHtmlVersion(int value)](#setHtmlVersion-int-) | Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. |
| [getExportRoundtripInformation()](#getExportRoundtripInformation--) | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. |
| [setExportRoundtripInformation(boolean value)](#setExportRoundtripInformation-boolean-) | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. |
| [getResourceFolder()](#getResourceFolder--) | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. |
| [setResourceFolder(String value)](#setResourceFolder-java.lang.String-) | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. |
| [getResourceFolderAlias()](#getResourceFolderAlias--) | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. |
| [setResourceFolderAlias(String value)](#setResourceFolderAlias-java.lang.String-) | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. |
| [getFontsFolder()](#getFontsFolder--) | Specifies the physical folder where fonts are saved when exporting a document to HTML. |
| [setFontsFolder(String value)](#setFontsFolder-java.lang.String-) | Specifies the physical folder where fonts are saved when exporting a document to HTML. |
| [getFontsFolderAlias()](#getFontsFolderAlias--) | Specifies the name of the folder used to construct font URIs written into an HTML document. |
| [setFontsFolderAlias(String value)](#setFontsFolderAlias-java.lang.String-) | Specifies the name of the folder used to construct font URIs written into an HTML document. |
| [getFontResourcesSubsettingSizeThreshold()](#getFontResourcesSubsettingSizeThreshold--) | Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. |
| [setFontResourcesSubsettingSizeThreshold(int value)](#setFontResourcesSubsettingSizeThreshold-int-) | Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. |
| [getFontSavingCallback()](#getFontSavingCallback--) | Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB. |
| [setFontSavingCallback(IFontSavingCallback value)](#setFontSavingCallback-com.aspose.words.IFontSavingCallback-) | Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB. |
| [getImagesFolder()](#getImagesFolder--) | Specifies the physical folder where images are saved when exporting a document to HTML format. |
| [setImagesFolder(String value)](#setImagesFolder-java.lang.String-) | Specifies the physical folder where images are saved when exporting a document to HTML format. |
| [getImagesFolderAlias()](#getImagesFolderAlias--) | Specifies the name of the folder used to construct image URIs written into an HTML document. |
| [setImagesFolderAlias(String value)](#setImagesFolderAlias-java.lang.String-) | Specifies the name of the folder used to construct image URIs written into an HTML document. |
| [getImageResolution()](#getImageResolution--) | Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. |
| [setImageResolution(int value)](#setImageResolution-int-) | Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. |
| [getImageSavingCallback()](#getImageSavingCallback--) | Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB. |
| [setImageSavingCallback(IImageSavingCallback value)](#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) | Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB. |
| [getScaleImageToShapeSize()](#getScaleImageToShapeSize--) | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. |
| [setScaleImageToShapeSize(boolean value)](#setScaleImageToShapeSize-boolean-) | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. |
| [getTableWidthOutputMode()](#getTableWidthOutputMode--) | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. |
| [setTableWidthOutputMode(int value)](#setTableWidthOutputMode-int-) | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. |
| [getOfficeMathOutputMode()](#getOfficeMathOutputMode--) | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. |
| [setOfficeMathOutputMode(int value)](#setOfficeMathOutputMode-int-) | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. |
| [getExportOriginalUrlForLinkedImages()](#getExportOriginalUrlForLinkedImages--) | Specifies whether original URL should be used as the URL of the linked images. |
| [setExportOriginalUrlForLinkedImages(boolean value)](#setExportOriginalUrlForLinkedImages-boolean-) | Specifies whether original URL should be used as the URL of the linked images. |
| [getExportCidUrlsForMhtmlResources()](#getExportCidUrlsForMhtmlResources--) | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. |
| [setExportCidUrlsForMhtmlResources(boolean value)](#setExportCidUrlsForMhtmlResources-boolean-) | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. |
| [getResolveFontNames()](#getResolveFontNames--) | Specifies whether font family names used in the document are resolved and substituted according to [Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) when being written into HTML-based formats. |
| [setResolveFontNames(boolean value)](#setResolveFontNames-boolean-) | Specifies whether font family names used in the document are resolved and substituted according to [Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) when being written into HTML-based formats. |
### HtmlSaveOptions() {#HtmlSaveOptions--}
```
public HtmlSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML) format.

### HtmlSaveOptions(int saveFormat) {#HtmlSaveOptions-int-}
```
public HtmlSaveOptions(int saveFormat)
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


Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getAllowNegativeIndent() {#getAllowNegativeIndent--}
```
public boolean getAllowNegativeIndent()
```


Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is  false .

When negative indent is not allowed, it is exported as zero margin to HTML. When negative indent is allowed, a paragraph might appear partially outside of the browser window.

**Returns:**
boolean - The corresponding  boolean  value.
### setAllowNegativeIndent(boolean value) {#setAllowNegativeIndent-boolean-}
```
public void setAllowNegativeIndent(boolean value)
```


Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is  false .

When negative indent is not allowed, it is exported as zero margin to HTML. When negative indent is allowed, a paragraph might appear partially outside of the browser window.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getCssStyleSheetFileName() {#getCssStyleSheetFileName--}
```
public String getCssStyleSheetFileName()
```


Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string.

This property has effect only when saving a document to HTML format and external CSS style sheet is requested using [getCssStyleSheetType()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetType--) / [setCssStyleSheetType(int)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetType-int-).

If this property is empty, the CSS file will be saved into the same folder and with the same name as the HTML document but with the ".css" extension.

If only path but no file name is specified in this property, the CSS file will be saved into the specified folder and will have the same name as the HTML document but with the ".css" extension.

If the folder specified by this property doesn't exist, it will be created automatically before the CSS file is saved.

Another way to specify a folder where external CSS file is saved is to use [getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setCssStyleSheetFileName(String value) {#setCssStyleSheetFileName-java.lang.String-}
```
public void setCssStyleSheetFileName(String value)
```


Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string.

This property has effect only when saving a document to HTML format and external CSS style sheet is requested using [getCssStyleSheetType()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetType--) / [setCssStyleSheetType(int)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetType-int-).

If this property is empty, the CSS file will be saved into the same folder and with the same name as the HTML document but with the ".css" extension.

If only path but no file name is specified in this property, the CSS file will be saved into the specified folder and will have the same name as the HTML document but with the ".css" extension.

If the folder specified by this property doesn't exist, it will be created automatically before the CSS file is saved.

Another way to specify a folder where external CSS file is saved is to use [getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getCssStyleSheetType() {#getCssStyleSheetType--}
```
public int getCssStyleSheetType()
```


Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [CssStyleSheetType.INLINE](../../com.aspose.words/cssstylesheettype\#INLINE) for HTML/MHTML and [CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL) for EPUB.

Saving CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL), CSS file will be encapsulated into the output package.

**Returns:**
int - The corresponding  int  value. The returned value is one of [CssStyleSheetType](../../com.aspose.words/cssstylesheettype) constants.
### setCssStyleSheetType(int value) {#setCssStyleSheetType-int-}
```
public void setCssStyleSheetType(int value)
```


Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [CssStyleSheetType.INLINE](../../com.aspose.words/cssstylesheettype\#INLINE) for HTML/MHTML and [CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL) for EPUB.

Saving CSS style sheet into an external file is only supported when saving to HTML. When you are exporting to one of the container formats (EPUB or MHTML) and specifying [CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL), CSS file will be encapsulated into the output package.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [CssStyleSheetType](../../com.aspose.words/cssstylesheettype) constants. |

### getCssClassNamePrefix() {#getCssClassNamePrefix--}
```
public String getCssClassNamePrefix()
```


Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix.

If this value is not empty, all CSS classes generated by Aspose.Words will start with the specified prefix. This might be useful, for example, if you add custom CSS to generated documents and want to prevent class name conflicts.

If the value is not  null  or empty, it must be a valid CSS identifier.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setCssClassNamePrefix(String value) {#setCssClassNamePrefix-java.lang.String-}
```
public void setCssClassNamePrefix(String value)
```


Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix.

If this value is not empty, all CSS classes generated by Aspose.Words will start with the specified prefix. This might be useful, for example, if you add custom CSS to generated documents and want to prevent class name conflicts.

If the value is not  null  or empty, it must be a valid CSS identifier.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getDocumentPartSavingCallback() {#getDocumentPartSavingCallback--}
```
public IDocumentPartSavingCallback getDocumentPartSavingCallback()
```


Allows to control how document parts are saved when a document is saved to HTML or EPUB.

**Returns:**
[IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback) - The corresponding [IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback) value.
### setDocumentPartSavingCallback(IDocumentPartSavingCallback value) {#setDocumentPartSavingCallback-com.aspose.words.IDocumentPartSavingCallback-}
```
public void setDocumentPartSavingCallback(IDocumentPartSavingCallback value)
```


Allows to control how document parts are saved when a document is saved to HTML or EPUB.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback) | The corresponding [IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback) value. |

### getCssSavingCallback() {#getCssSavingCallback--}
```
public ICssSavingCallback getCssSavingCallback()
```


Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB.

**Returns:**
[ICssSavingCallback](../../com.aspose.words/icsssavingcallback) - The corresponding [ICssSavingCallback](../../com.aspose.words/icsssavingcallback) value.
### setCssSavingCallback(ICssSavingCallback value) {#setCssSavingCallback-com.aspose.words.ICssSavingCallback-}
```
public void setCssSavingCallback(ICssSavingCallback value)
```


Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [ICssSavingCallback](../../com.aspose.words/icsssavingcallback) | The corresponding [ICssSavingCallback](../../com.aspose.words/icsssavingcallback) value. |

### getDocumentSplitCriteria() {#getDocumentSplitCriteria--}
```
public int getDocumentSplitCriteria()
```


Specifies how the document should be split when saving to [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) format. Default is [DocumentSplitCriteria.NONE](../../com.aspose.words/documentsplitcriteria\#NONE) for HTML and [DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH) for EPUB and AZW3.

Normally you would want a document saved to HTML as a single file. But in some cases it is preferable to split the output into several smaller HTML pages. When saving to HTML format these pages will be output to individual files or streams. When saving to EPUB format they will be incorporated into corresponding packages.

A document cannot be split when saving in the MHTML format.

**Returns:**
int - The corresponding  int  value. The returned value is a bitwise combination of [DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria) constants.
### setDocumentSplitCriteria(int value) {#setDocumentSplitCriteria-int-}
```
public void setDocumentSplitCriteria(int value)
```


Specifies how the document should be split when saving to [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) or [SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) format. Default is [DocumentSplitCriteria.NONE](../../com.aspose.words/documentsplitcriteria\#NONE) for HTML and [DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH) for EPUB and AZW3.

Normally you would want a document saved to HTML as a single file. But in some cases it is preferable to split the output into several smaller HTML pages. When saving to HTML format these pages will be output to individual files or streams. When saving to EPUB format they will be incorporated into corresponding packages.

A document cannot be split when saving in the MHTML format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be a bitwise combination of [DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria) constants. |

### getDocumentSplitHeadingLevel() {#getDocumentSplitHeadingLevel--}
```
public int getDocumentSplitHeadingLevel()
```


Specifies the maximum level of headings at which to split the document. Default value is  2 .

When [getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions\#getDocumentSplitCriteria--) / [setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions\#setDocumentSplitCriteria-int-) includes [DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH) and this property is set to a value from 1 to 9, the document will be split at paragraphs formatted using **Heading 1**, **Heading 2** , **Heading 3** etc. styles up to the specified heading level.

By default, only **Heading 1** and **Heading 2** paragraphs cause the document to be split. Setting this property to zero will cause the document not to be split at heading paragraphs at all.

**Returns:**
int - The corresponding  int  value.
### setDocumentSplitHeadingLevel(int value) {#setDocumentSplitHeadingLevel-int-}
```
public void setDocumentSplitHeadingLevel(int value)
```


Specifies the maximum level of headings at which to split the document. Default value is  2 .

When [getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions\#getDocumentSplitCriteria--) / [setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions\#setDocumentSplitCriteria-int-) includes [DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH) and this property is set to a value from 1 to 9, the document will be split at paragraphs formatted using **Heading 1**, **Heading 2** , **Heading 3** etc. styles up to the specified heading level.

By default, only **Heading 1** and **Heading 2** paragraphs cause the document to be split. Setting this property to zero will cause the document not to be split at heading paragraphs at all.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```




**Returns:**
java.nio.charset.Charset
### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset-}
```
public void setEncoding(Charset value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.nio.charset.Charset |  |

### getEpubNavigationMapLevel() {#getEpubNavigationMapLevel--}
```
public int getEpubNavigationMapLevel()
```


Specifies the maximum level of headings populated to the navigation map when exporting to IDPF EPUB format. Default value is  3 .

Navigation map in IDPF EPUB format allows user agents to provide easy way of navigation through the document structure. Usually navigation points correspond to headings in the document. To populate headings up to level **N** assign this value to [getEpubNavigationMapLevel()](../../com.aspose.words/htmlsaveoptions\#getEpubNavigationMapLevel--) / [setEpubNavigationMapLevel(int)](../../com.aspose.words/htmlsaveoptions\#setEpubNavigationMapLevel-int-).

By default, three levels of headings are populated: paragraphs of styles **Heading 1**, **Heading 2** and **Heading 3**. You can set this property to a value from 1 to 9 to request corresponding maximum level. Setting it to zero will reduce navigation map to only document root or roots of document parts.

**Returns:**
int - The corresponding  int  value.
### setEpubNavigationMapLevel(int value) {#setEpubNavigationMapLevel-int-}
```
public void setEpubNavigationMapLevel(int value)
```


Specifies the maximum level of headings populated to the navigation map when exporting to IDPF EPUB format. Default value is  3 .

Navigation map in IDPF EPUB format allows user agents to provide easy way of navigation through the document structure. Usually navigation points correspond to headings in the document. To populate headings up to level **N** assign this value to [getEpubNavigationMapLevel()](../../com.aspose.words/htmlsaveoptions\#getEpubNavigationMapLevel--) / [setEpubNavigationMapLevel(int)](../../com.aspose.words/htmlsaveoptions\#setEpubNavigationMapLevel-int-).

By default, three levels of headings are populated: paragraphs of styles **Heading 1**, **Heading 2** and **Heading 3**. You can set this property to a value from 1 to 9 to request corresponding maximum level. Setting it to zero will reduce navigation map to only document root or roots of document parts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getExportDocumentProperties() {#getExportDocumentProperties--}
```
public boolean getExportDocumentProperties()
```


Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### setExportDocumentProperties(boolean value) {#setExportDocumentProperties-boolean-}
```
public void setExportDocumentProperties(boolean value)
```


Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportFontResources() {#getExportFontResources--}
```
public boolean getExportFontResources()
```


Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is  false .

Exporting font resources allows for consistent document rendering independent of the fonts available in a given user's environment.

If [getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) is set to  true , main HTML document will refer to every font via the CSS 3 **@font-face** at-rule and fonts will be output as separate files. When exporting to IDPF EPUB or MHTML formats, fonts will be embedded into the corresponding package along with other subsidiary files.

If [getExportFontsAsBase64()](../../com.aspose.words/htmlsaveoptions\#getExportFontsAsBase64--) / [setExportFontsAsBase64(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontsAsBase64-boolean-) is set to  true , fonts will not be saved to separate files. Instead, they will be embedded into **@font-face** at-rules in Base64 encoding.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules in CSS style sheets is not allowed. Font subsetting can also violate license terms.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportFontResources(boolean value) {#setExportFontResources-boolean-}
```
public void setExportFontResources(boolean value)
```


Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is  false .

Exporting font resources allows for consistent document rendering independent of the fonts available in a given user's environment.

If [getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) is set to  true , main HTML document will refer to every font via the CSS 3 **@font-face** at-rule and fonts will be output as separate files. When exporting to IDPF EPUB or MHTML formats, fonts will be embedded into the corresponding package along with other subsidiary files.

If [getExportFontsAsBase64()](../../com.aspose.words/htmlsaveoptions\#getExportFontsAsBase64--) / [setExportFontsAsBase64(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontsAsBase64-boolean-) is set to  true , fonts will not be saved to separate files. Instead, they will be embedded into **@font-face** at-rules in Base64 encoding.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules in CSS style sheets is not allowed. Font subsetting can also violate license terms.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportFontsAsBase64() {#getExportFontsAsBase64--}
```
public boolean getExportFontsAsBase64()
```


Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is  false .

By default, fonts are written to separate files. If this option is set to  true , fonts will be embedded into the document's CSS in Base64 encoding.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportFontsAsBase64(boolean value) {#setExportFontsAsBase64-boolean-}
```
public void setExportFontsAsBase64(boolean value)
```


Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is  false .

By default, fonts are written to separate files. If this option is set to  true , fonts will be embedded into the document's CSS in Base64 encoding.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportHeadersFootersMode() {#getExportHeadersFootersMode--}
```
public int getExportHeadersFootersMode()
```


Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is [ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION) for HTML/MHTML and [ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE) for EPUB.

It is hard to meaningfully output headers and footers to HTML because HTML is not paginated.

When this property is [ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION), Aspose.Words exports only primary headers and footers at the beginning and the end of each section.

When it is [ExportHeadersFootersMode.FIRST\_SECTION\_HEADER\_LAST\_SECTION\_FOOTER](../../com.aspose.words/exportheadersfootersmode\#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) only first primary header and the last primary footer (including linked to previous) are exported.

You can disable export of headers and footers altogether by setting this property to [ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE).

**Returns:**
int - The corresponding  int  value. The returned value is one of [ExportHeadersFootersMode](../../com.aspose.words/exportheadersfootersmode) constants.
### setExportHeadersFootersMode(int value) {#setExportHeadersFootersMode-int-}
```
public void setExportHeadersFootersMode(int value)
```


Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is [ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION) for HTML/MHTML and [ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE) for EPUB.

It is hard to meaningfully output headers and footers to HTML because HTML is not paginated.

When this property is [ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION), Aspose.Words exports only primary headers and footers at the beginning and the end of each section.

When it is [ExportHeadersFootersMode.FIRST\_SECTION\_HEADER\_LAST\_SECTION\_FOOTER](../../com.aspose.words/exportheadersfootersmode\#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) only first primary header and the last primary footer (including linked to previous) are exported.

You can disable export of headers and footers altogether by setting this property to [ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ExportHeadersFootersMode](../../com.aspose.words/exportheadersfootersmode) constants. |

### getExportImagesAsBase64() {#getExportImagesAsBase64--}
```
public boolean getExportImagesAsBase64()
```


Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is  false .

When this property is set to  true  images data are exported directly into the **img** elements and separate files are not created.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportImagesAsBase64(boolean value) {#setExportImagesAsBase64-boolean-}
```
public void setExportImagesAsBase64(boolean value)
```


Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is  false .

When this property is set to  true  images data are exported directly into the **img** elements and separate files are not created.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportLanguageInformation() {#getExportLanguageInformation--}
```
public boolean getExportLanguageInformation()
```


Specifies whether language information is exported to HTML, MHTML or EPUB. Default is  false .

When this property is set to  true  Aspose.Words outputs **lang** HTML attribute on the document elements that specify language. This can be needed to preserve language related semantics.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportLanguageInformation(boolean value) {#setExportLanguageInformation-boolean-}
```
public void setExportLanguageInformation(boolean value)
```


Specifies whether language information is exported to HTML, MHTML or EPUB. Default is  false .

When this property is set to  true  Aspose.Words outputs **lang** HTML attribute on the document elements that specify language. This can be needed to preserve language related semantics.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportListLabels() {#getExportListLabels--}
```
public int getExportListLabels()
```


Controls how list labels are output to HTML, MHTML or EPUB. Default value is [ExportListLabels.AUTO](../../com.aspose.words/exportlistlabels\#AUTO).

**Returns:**
int - The corresponding  int  value. The returned value is one of [ExportListLabels](../../com.aspose.words/exportlistlabels) constants.
### setExportListLabels(int value) {#setExportListLabels-int-}
```
public void setExportListLabels(int value)
```


Controls how list labels are output to HTML, MHTML or EPUB. Default value is [ExportListLabels.AUTO](../../com.aspose.words/exportlistlabels\#AUTO).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [ExportListLabels](../../com.aspose.words/exportlistlabels) constants. |

### getMetafileFormat() {#getMetafileFormat--}
```
public int getMetafileFormat()
```


Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is [HtmlMetafileFormat.PNG](../../com.aspose.words/htmlmetafileformat\#PNG), meaning that metafiles are rendered to raster PNG images.

Metafiles are not natively displayed by HTML browsers. By default, Aspose.Words converts WMF and EMF images into PNG files when exporting to HTML. Other options are to convert metafiles to SVG images or to export them as is without conversion.

Some image transforms, in particular image cropping, will not be applied to metafile images if they are exported to HTML without conversion.

**Returns:**
int - The corresponding  int  value. The returned value is one of [HtmlMetafileFormat](../../com.aspose.words/htmlmetafileformat) constants.
### setMetafileFormat(int value) {#setMetafileFormat-int-}
```
public void setMetafileFormat(int value)
```


Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is [HtmlMetafileFormat.PNG](../../com.aspose.words/htmlmetafileformat\#PNG), meaning that metafiles are rendered to raster PNG images.

Metafiles are not natively displayed by HTML browsers. By default, Aspose.Words converts WMF and EMF images into PNG files when exporting to HTML. Other options are to convert metafiles to SVG images or to export them as is without conversion.

Some image transforms, in particular image cropping, will not be applied to metafile images if they are exported to HTML without conversion.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HtmlMetafileFormat](../../com.aspose.words/htmlmetafileformat) constants. |

### getExportPageSetup() {#getExportPageSetup--}
```
public boolean getExportPageSetup()
```


Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is  false .

Each [Section](../../com.aspose.words/section) in Aspose.Words document model provides page setup information via [PageSetup](../../com.aspose.words/pagesetup) class. When you export a document to HTML format you might need to keep this information for further usage. In particular, page setup might be important for rendering to paged media (printing) or subsequent conversion to the native Microsoft Word file formats (DOCX, DOC, RTF, WML).

In most cases HTML is intended for viewing in browsers where pagination is not performed. So this feature is inactive by default.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportPageSetup(boolean value) {#setExportPageSetup-boolean-}
```
public void setExportPageSetup(boolean value)
```


Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is  false .

Each [Section](../../com.aspose.words/section) in Aspose.Words document model provides page setup information via [PageSetup](../../com.aspose.words/pagesetup) class. When you export a document to HTML format you might need to keep this information for further usage. In particular, page setup might be important for rendering to paged media (printing) or subsequent conversion to the native Microsoft Word file formats (DOCX, DOC, RTF, WML).

In most cases HTML is intended for viewing in browsers where pagination is not performed. So this feature is inactive by default.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportPageMargins() {#getExportPageMargins--}
```
public boolean getExportPageMargins()
```


Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is  false . Aspose.Words does not show area of page margins by default. If any elements are completely or partially clipped by the document edge the displayed area can be extended with this option.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportPageMargins(boolean value) {#setExportPageMargins-boolean-}
```
public void setExportPageMargins(boolean value)
```


Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is  false . Aspose.Words does not show area of page margins by default. If any elements are completely or partially clipped by the document edge the displayed area can be extended with this option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportRelativeFontSize() {#getExportRelativeFontSize--}
```
public boolean getExportRelativeFontSize()
```


Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is  false .

In many existing documents (HTML, IDPF EPUB) font sizes are specified in relative units. This allows applications to adjust text size when viewing/processing documents. For instance, Microsoft Internet Explorer has "View->Text Size" submenu, Adobe Digital Editions has two buttons: Increase/Decrease Text Size. If you expect this functionality to work then set [getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-) property to  true .

Aspose Words document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. Font size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **1.5em.** to the HTML.

When this option is enabled, document elements other than text will still have absolute sizes. Also some text-related attributes might be expressed absolutely. In particular, line spacing specified with "exactly" rule might produce unwanted results when scaling text. So the source documents should be properly designed and tested when exporting with [getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-) set to  true .

**Returns:**
boolean - The corresponding  boolean  value.
### setExportRelativeFontSize(boolean value) {#setExportRelativeFontSize-boolean-}
```
public void setExportRelativeFontSize(boolean value)
```


Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is  false .

In many existing documents (HTML, IDPF EPUB) font sizes are specified in relative units. This allows applications to adjust text size when viewing/processing documents. For instance, Microsoft Internet Explorer has "View->Text Size" submenu, Adobe Digital Editions has two buttons: Increase/Decrease Text Size. If you expect this functionality to work then set [getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-) property to  true .

Aspose Words document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. Font size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **1.5em.** to the HTML.

When this option is enabled, document elements other than text will still have absolute sizes. Also some text-related attributes might be expressed absolutely. In particular, line spacing specified with "exactly" rule might produce unwanted results when scaling text. So the source documents should be properly designed and tested when exporting with [getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-) set to  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportTextInputFormFieldAsText() {#getExportTextInputFormFieldAsText--}
```
public boolean getExportTextInputFormFieldAsText()
```


Controls how text input form fields are saved to HTML or MHTML. Default value is  false .

When set to  true , exports text input form fields as normal text. When  false , exports Word text input form fields as INPUT elements in HTML.

When exporting to EPUB, text input form fields are always saved as text due to requirements of this format.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportTextInputFormFieldAsText(boolean value) {#setExportTextInputFormFieldAsText-boolean-}
```
public void setExportTextInputFormFieldAsText(boolean value)
```


Controls how text input form fields are saved to HTML or MHTML. Default value is  false .

When set to  true , exports text input form fields as normal text. When  false , exports Word text input form fields as INPUT elements in HTML.

When exporting to EPUB, text input form fields are always saved as text due to requirements of this format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportShapesAsSvg() {#getExportShapesAsSvg--}
```
public boolean getExportShapesAsSvg()
```


Controls whether [Shape](../../com.aspose.words/shape) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is  false .

If this option is set to  true , [Shape](../../com.aspose.words/shape) nodes are exported as  elements. Otherwise, they are rendered to bitmaps and are exported as ![Image 1][] elements.


[Image 1]: 

**Returns:**
boolean - The corresponding  boolean  value.
### setExportShapesAsSvg(boolean value) {#setExportShapesAsSvg-boolean-}
```
public void setExportShapesAsSvg(boolean value)
```


Controls whether [Shape](../../com.aspose.words/shape) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is  false .

If this option is set to  true , [Shape](../../com.aspose.words/shape) nodes are exported as  elements. Otherwise, they are rendered to bitmaps and are exported as ![Image 1][] elements.


[Image 1]: 

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportDropDownFormFieldAsText() {#getExportDropDownFormFieldAsText--}
```
public boolean getExportDropDownFormFieldAsText()
```


Controls how drop-down form fields are saved to HTML or MHTML. Default value is  false .

When set to  true , exports drop-down form fields as normal text. When  false , exports drop-down form fields as SELECT element in HTML.

When exporting to EPUB, text drop-down form fields are always saved as text due to requirements of this format.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportDropDownFormFieldAsText(boolean value) {#setExportDropDownFormFieldAsText-boolean-}
```
public void setExportDropDownFormFieldAsText(boolean value)
```


Controls how drop-down form fields are saved to HTML or MHTML. Default value is  false .

When set to  true , exports drop-down form fields as normal text. When  false , exports drop-down form fields as SELECT element in HTML.

When exporting to EPUB, text drop-down form fields are always saved as text due to requirements of this format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportTocPageNumbers() {#getExportTocPageNumbers--}
```
public boolean getExportTocPageNumbers()
```


Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### setExportTocPageNumbers(boolean value) {#setExportTocPageNumbers-boolean-}
```
public void setExportTocPageNumbers(boolean value)
```


Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportXhtmlTransitional() {#getExportXhtmlTransitional--}
```
public boolean getExportXhtmlTransitional()
```


Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When  true , writes a DOCTYPE declaration in the document prior to the root element. Default value is  false . When saving to EPUB or HTML5 ( [HtmlVersion.HTML\_5](../../com.aspose.words/htmlversion\#HTML-5)) the DOCTYPE declaration is always written.

Aspose.Words always writes well formed HTML regardless of this setting.

When  true , the beginning of the HTML output document will look like this:

```

 
 
 
 
```

Aspose.Words aims to output XHTML according to the XHTML 1.0 Transitional specification, but the output will not always validate against the DTD. Some structures inside a Microsoft Word document are hard or impossible to map to a document that will validate against the XHTML schema. For example, XHTML does not allow nested lists (UL cannot be nested inside another UL element), but in Microsoft Word document multilevel lists occur quite often.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportXhtmlTransitional(boolean value) {#setExportXhtmlTransitional-boolean-}
```
public void setExportXhtmlTransitional(boolean value)
```


Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When  true , writes a DOCTYPE declaration in the document prior to the root element. Default value is  false . When saving to EPUB or HTML5 ( [HtmlVersion.HTML\_5](../../com.aspose.words/htmlversion\#HTML-5)) the DOCTYPE declaration is always written.

Aspose.Words always writes well formed HTML regardless of this setting.

When  true , the beginning of the HTML output document will look like this:

```

 
 
 
 
```

Aspose.Words aims to output XHTML according to the XHTML 1.0 Transitional specification, but the output will not always validate against the DTD. Some structures inside a Microsoft Word document are hard or impossible to map to a document that will validate against the XHTML schema. For example, XHTML does not allow nested lists (UL cannot be nested inside another UL element), but in Microsoft Word document multilevel lists occur quite often.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getHtmlVersion() {#getHtmlVersion--}
```
public int getHtmlVersion()
```


Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is [HtmlVersion.XHTML](../../com.aspose.words/htmlversion\#XHTML).

**Returns:**
int - The corresponding  int  value. The returned value is one of [HtmlVersion](../../com.aspose.words/htmlversion) constants.
### setHtmlVersion(int value) {#setHtmlVersion-int-}
```
public void setHtmlVersion(int value)
```


Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is [HtmlVersion.XHTML](../../com.aspose.words/htmlversion\#XHTML).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HtmlVersion](../../com.aspose.words/htmlversion) constants. |

### getExportRoundtripInformation() {#getExportRoundtripInformation--}
```
public boolean getExportRoundtripInformation()
```


Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is  true  for HTML and  false  for MHTML and EPUB.

Saving of the roundtrip information allows to restore document properties such as tab stops, comments, headers and footers during the HTML documents loading back into a [Document](../../com.aspose.words/document) object.

When  true , the roundtrip information is exported as -aw-\* CSS properties of the corresponding HTML elements.

When  false , causes no roundtrip information to be output into produced files.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportRoundtripInformation(boolean value) {#setExportRoundtripInformation-boolean-}
```
public void setExportRoundtripInformation(boolean value)
```


Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is  true  for HTML and  false  for MHTML and EPUB.

Saving of the roundtrip information allows to restore document properties such as tab stops, comments, headers and footers during the HTML documents loading back into a [Document](../../com.aspose.words/document) object.

When  true , the roundtrip information is exported as -aw-\* CSS properties of the corresponding HTML elements.

When  false , causes no roundtrip information to be output into produced files.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getResourceFolder() {#getResourceFolder--}
```
public String getResourceFolder()
```


Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) is the simplest way to specify a folder where all resources should be written. Another way is to use individual properties [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-), and [getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-).

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) has a lower priority than folders specified via [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-), and [getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-). For example, if both [getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) and [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) are specified, fonts will be saved to [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), while images and CSS will be saved to [getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

If the folder specified by [getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) doesn't exist, it will be created automatically.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setResourceFolder(String value) {#setResourceFolder-java.lang.String-}
```
public void setResourceFolder(String value)
```


Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) is the simplest way to specify a folder where all resources should be written. Another way is to use individual properties [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-), and [getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-).

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) has a lower priority than folders specified via [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-), and [getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-). For example, if both [getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) and [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) are specified, fonts will be saved to [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), while images and CSS will be saved to [getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

If the folder specified by [getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) doesn't exist, it will be created automatically.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getResourceFolderAlias() {#getResourceFolderAlias--}
```
public String getResourceFolderAlias()
```


Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string.

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) is the simplest way to specify how URIs for all resource files should be constructed. Same information can be specified for images and fonts separately via [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) properties, respectively. However, there is no individual property for CSS.

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) has lower priority than [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-). For example, if both [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) are specified, fonts' URIs will be constructed using [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-), while URIs of images and CSS will be constructed using [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

If [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) is empty, the [getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) property value will be used to construct resource URIs.

If [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) is set to '.' (dot), resource URIs will contain file names only, without any path.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setResourceFolderAlias(String value) {#setResourceFolderAlias-java.lang.String-}
```
public void setResourceFolderAlias(String value)
```


Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string.

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) is the simplest way to specify how URIs for all resource files should be constructed. Same information can be specified for images and fonts separately via [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) properties, respectively. However, there is no individual property for CSS.

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) has lower priority than [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-). For example, if both [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) are specified, fonts' URIs will be constructed using [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-), while URIs of images and CSS will be constructed using [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

If [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) is empty, the [getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) property value will be used to construct resource URIs.

If [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) is set to '.' (dot), resource URIs will contain file names only, without any path.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getFontsFolder() {#getFontsFolder--}
```
public String getFontsFolder()
```


Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in HTML format and [getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) is set to  true , Aspose.Words needs to save fonts used in the document as standalone files. [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) allows you to specify where the fonts will be saved and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) allows to specify how the font URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the fonts in the same folder where the document file is saved. Use [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the fonts, but still needs to save the fonts somewhere. In this case, you need to specify an accessible folder in the [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) property or provide custom streams via the [getFontSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getFontSavingCallback--) / [setFontSavingCallback(com.aspose.words.IFontSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setFontSavingCallback-com.aspose.words.IFontSavingCallback-) event handler.

If the folder specified by [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) doesn't exist, it will be created automatically.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) is another way to specify a folder where fonts should be saved.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setFontsFolder(String value) {#setFontsFolder-java.lang.String-}
```
public void setFontsFolder(String value)
```


Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in HTML format and [getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) is set to  true , Aspose.Words needs to save fonts used in the document as standalone files. [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) allows you to specify where the fonts will be saved and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) allows to specify how the font URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the fonts in the same folder where the document file is saved. Use [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the fonts, but still needs to save the fonts somewhere. In this case, you need to specify an accessible folder in the [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) property or provide custom streams via the [getFontSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getFontSavingCallback--) / [setFontSavingCallback(com.aspose.words.IFontSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setFontSavingCallback-com.aspose.words.IFontSavingCallback-) event handler.

If the folder specified by [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) doesn't exist, it will be created automatically.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) is another way to specify a folder where fonts should be saved.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getFontsFolderAlias() {#getFontsFolderAlias--}
```
public String getFontsFolderAlias()
```


Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in HTML format and [getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) is set to  true , Aspose.Words needs to save fonts used in the document as standalone files. [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) allows you to specify where the fonts will be saved and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) allows to specify how the font URIs will be constructed.

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) is not an empty string, then the font URI written to HTML will be *FontsFolderAlias +* . 

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) is an empty string, then the font URI written to HTML will be *FontsFolder +* . 

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) is set to '.' (dot), then the font file name will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct font URIs is to use [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setFontsFolderAlias(String value) {#setFontsFolderAlias-java.lang.String-}
```
public void setFontsFolderAlias(String value)
```


Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in HTML format and [getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) is set to  true , Aspose.Words needs to save fonts used in the document as standalone files. [getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) allows you to specify where the fonts will be saved and [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) allows to specify how the font URIs will be constructed.

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) is not an empty string, then the font URI written to HTML will be *FontsFolderAlias +* . 

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) is an empty string, then the font URI written to HTML will be *FontsFolder +* . 

If [getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) is set to '.' (dot), then the font file name will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct font URIs is to use [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getFontResourcesSubsettingSizeThreshold() {#getFontResourcesSubsettingSizeThreshold--}
```
public int getFontResourcesSubsettingSizeThreshold()
```


Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is  0 .

[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. Font subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

Font subsetting works as follows:

 *  By default, all exported fonts are subsetted.
 *  Setting [getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
 *  Setting the property to  suppresses font subsetting.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules in CSS style sheets is not allowed. Font subsetting can also violate license terms.

**Returns:**
int - The corresponding  int  value.
### setFontResourcesSubsettingSizeThreshold(int value) {#setFontResourcesSubsettingSizeThreshold-int-}
```
public void setFontResourcesSubsettingSizeThreshold(int value)
```


Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is  0 .

[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. Font subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

Font subsetting works as follows:

 *  By default, all exported fonts are subsetted.
 *  Setting [getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
 *  Setting the property to  suppresses font subsetting.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules in CSS style sheets is not allowed. Font subsetting can also violate license terms.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getFontSavingCallback() {#getFontSavingCallback--}
```
public IFontSavingCallback getFontSavingCallback()
```


Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB.

**Returns:**
[IFontSavingCallback](../../com.aspose.words/ifontsavingcallback) - The corresponding [IFontSavingCallback](../../com.aspose.words/ifontsavingcallback) value.
### setFontSavingCallback(IFontSavingCallback value) {#setFontSavingCallback-com.aspose.words.IFontSavingCallback-}
```
public void setFontSavingCallback(IFontSavingCallback value)
```


Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IFontSavingCallback](../../com.aspose.words/ifontsavingcallback) | The corresponding [IFontSavingCallback](../../com.aspose.words/ifontsavingcallback) value. |

### getImagesFolder() {#getImagesFolder--}
```
public String getImagesFolder()
```


Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) property or provide custom streams via the [getImageSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getImageSavingCallback--) / [setImageSavingCallback(com.aspose.words.IImageSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) event handler.

If the folder specified by [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) doesn't exist, it will be created automatically.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) is another way to specify a folder where images should be saved.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setImagesFolder(String value) {#setImagesFolder-java.lang.String-}
```
public void setImagesFolder(String value)
```


Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) property or provide custom streams via the [getImageSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getImageSavingCallback--) / [setImageSavingCallback(com.aspose.words.IImageSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) event handler.

If the folder specified by [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) doesn't exist, it will be created automatically.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) is another way to specify a folder where images should be saved.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getImagesFolderAlias() {#getImagesFolderAlias--}
```
public String getImagesFolderAlias()
```


Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) is not an empty string, then the image URI written to HTML will be *ImagesFolderAlias + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) is an empty string, then the image URI written to HTML will be *ImagesFolder + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) is set to '.' (dot), then the image file name will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct image URIs is to use [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).


[Image 1]: 

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setImagesFolderAlias(String value) {#setImagesFolderAlias-java.lang.String-}
```
public void setImagesFolderAlias(String value)
```


Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string.

When you save a [Document](../../com.aspose.words/document) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) allows you to specify where the images will be saved and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) allows to specify how the image URIs will be constructed.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) is not an empty string, then the image URI written to HTML will be *ImagesFolderAlias + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) is an empty string, then the image URI written to HTML will be *ImagesFolder + ![Image 1][]*.

If [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) is set to '.' (dot), then the image file name will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct image URIs is to use [getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).


[Image 1]: 

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getImageResolution() {#getImageResolution--}
```
public int getImageResolution()
```


Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is  96 dpi .

This property effects raster images when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) is  true  and effects metafiles exported as raster images. Some image properties such as cropping or rotation require saving transformed images and in this case transformed images are created in the given resolution.

**Returns:**
int - The corresponding  int  value.
### setImageResolution(int value) {#setImageResolution-int-}
```
public void setImageResolution(int value)
```


Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is  96 dpi .

This property effects raster images when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) is  true  and effects metafiles exported as raster images. Some image properties such as cropping or rotation require saving transformed images and in this case transformed images are created in the given resolution.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getImageSavingCallback() {#getImageSavingCallback--}
```
public IImageSavingCallback getImageSavingCallback()
```


Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB.

**Returns:**
[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) - The corresponding [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) value.
### setImageSavingCallback(IImageSavingCallback value) {#setImageSavingCallback-com.aspose.words.IImageSavingCallback-}
```
public void setImageSavingCallback(IImageSavingCallback value)
```


Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) | The corresponding [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) value. |

### getScaleImageToShapeSize() {#getScaleImageToShapeSize--}
```
public boolean getScaleImageToShapeSize()
```


Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is  true .

An image in a Microsoft Word document is a shape. The shape has a size and the image has its own size. The sizes are not directly linked. For example, the image can be 1024x786 pixels, but shape that displays this image can be 400x300 points.

In order to display an image in the browser, it must be scaled to the shape size. The [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) property controls where the scaling of the image takes place: in Aspose.Words during export to HTML or in the browser when displaying the document.

When [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) is  true , the image is scaled by Aspose.Words using high quality scaling during export to HTML. When [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) is  false , the image is output with its original size and the browser has to scale it.

In general, browsers do quick and poor quality scaling. As a result, you will normally get better display quality in the browser and smaller file size when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) is  true , but better printing quality and faster conversion when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### setScaleImageToShapeSize(boolean value) {#setScaleImageToShapeSize-boolean-}
```
public void setScaleImageToShapeSize(boolean value)
```


Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is  true .

An image in a Microsoft Word document is a shape. The shape has a size and the image has its own size. The sizes are not directly linked. For example, the image can be 1024x786 pixels, but shape that displays this image can be 400x300 points.

In order to display an image in the browser, it must be scaled to the shape size. The [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) property controls where the scaling of the image takes place: in Aspose.Words during export to HTML or in the browser when displaying the document.

When [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) is  true , the image is scaled by Aspose.Words using high quality scaling during export to HTML. When [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) is  false , the image is output with its original size and the browser has to scale it.

In general, browsers do quick and poor quality scaling. As a result, you will normally get better display quality in the browser and smaller file size when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) is  true , but better printing quality and faster conversion when [getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getTableWidthOutputMode() {#getTableWidthOutputMode--}
```
public int getTableWidthOutputMode()
```


Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is [HtmlElementSizeOutputMode.ALL](../../com.aspose.words/htmlelementsizeoutputmode\#ALL).

In the HTML format, table, row and cell elements ( 

    | -- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | ,  | ) can have their widths specified either in relative (percentage) or in absolute units. In a document in Aspose.Words, tables, rows and cells can have their widths specified using either relative or absolute units too.  When you convert a document to HTML using Aspose.Words, you might want to control how table, row and cell widths are exported to affect how the resulting document is displayed in the visual agent (e.g. a browser or viewer).  Use this property as a filter to specify what table widths values are exported into the destination document. For example, if you are converting a document to EPUB and intend to view the document on a mobile reading device, then you probably want to avoid exporting absolute width values. To do this you need to specify the output mode [HtmlElementSizeOutputMode.RELATIVE\_ONLY](../../com.aspose.words/htmlelementsizeoutputmode\#RELATIVE-ONLY) or [HtmlElementSizeOutputMode.NONE](../../com.aspose.words/htmlelementsizeoutputmode\#NONE) so the viewer on the mobile device can layout the table to fit the width of the screen as best as it can. |

**Returns:**
int - The corresponding  int  value. The returned value is one of [HtmlElementSizeOutputMode](../../com.aspose.words/htmlelementsizeoutputmode) constants.
### setTableWidthOutputMode(int value) {#setTableWidthOutputMode-int-}
```
public void setTableWidthOutputMode(int value)
```


Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is [HtmlElementSizeOutputMode.ALL](../../com.aspose.words/htmlelementsizeoutputmode\#ALL).

In the HTML format, table, row and cell elements ( 

    | -- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | ,  | ) can have their widths specified either in relative (percentage) or in absolute units. In a document in Aspose.Words, tables, rows and cells can have their widths specified using either relative or absolute units too.  When you convert a document to HTML using Aspose.Words, you might want to control how table, row and cell widths are exported to affect how the resulting document is displayed in the visual agent (e.g. a browser or viewer).  Use this property as a filter to specify what table widths values are exported into the destination document. For example, if you are converting a document to EPUB and intend to view the document on a mobile reading device, then you probably want to avoid exporting absolute width values. To do this you need to specify the output mode [HtmlElementSizeOutputMode.RELATIVE\_ONLY](../../com.aspose.words/htmlelementsizeoutputmode\#RELATIVE-ONLY) or [HtmlElementSizeOutputMode.NONE](../../com.aspose.words/htmlelementsizeoutputmode\#NONE) so the viewer on the mobile device can layout the table to fit the width of the screen as best as it can. |

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HtmlElementSizeOutputMode](../../com.aspose.words/htmlelementsizeoutputmode) constants. |

### getOfficeMathOutputMode() {#getOfficeMathOutputMode--}
```
public int getOfficeMathOutputMode()
```


Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is  HtmlOfficeMathOutputMode.Image .

**Returns:**
int - The corresponding  int  value. The returned value is one of [HtmlOfficeMathOutputMode](../../com.aspose.words/htmlofficemathoutputmode) constants.
### setOfficeMathOutputMode(int value) {#setOfficeMathOutputMode-int-}
```
public void setOfficeMathOutputMode(int value)
```


Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is  HtmlOfficeMathOutputMode.Image .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HtmlOfficeMathOutputMode](../../com.aspose.words/htmlofficemathoutputmode) constants. |

### getExportOriginalUrlForLinkedImages() {#getExportOriginalUrlForLinkedImages--}
```
public boolean getExportOriginalUrlForLinkedImages()
```


Specifies whether original URL should be used as the URL of the linked images. Default value is  false .

If value is set to  true  [ImageData.getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) value is used as the URL of linked images and linked images are not loaded into document's folder or [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-).

If value is set to  false  linked images are loaded into document's folder or [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) and URL of each linked image is constructed depending on document's folder, [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) properties.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportOriginalUrlForLinkedImages(boolean value) {#setExportOriginalUrlForLinkedImages-boolean-}
```
public void setExportOriginalUrlForLinkedImages(boolean value)
```


Specifies whether original URL should be used as the URL of the linked images. Default value is  false .

If value is set to  true  [ImageData.getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) value is used as the URL of linked images and linked images are not loaded into document's folder or [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-).

If value is set to  false  linked images are loaded into document's folder or [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) and URL of each linked image is constructed depending on document's folder, [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) and [getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) properties.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getExportCidUrlsForMhtmlResources() {#getExportCidUrlsForMhtmlResources--}
```
public boolean getExportCidUrlsForMhtmlResources()
```


Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is  false .

This option affects only documents being saved to MHTML.

By default, resources in MHTML documents are referenced by file name (for example, "image.png"), which are matched against "Content-Location" headers of MIME parts.

This option enables an alternative method, where references to resource files are written as CID (Content-ID) URLs (for example, "cid:image.png") and are matched against "Content-ID" headers.

In theory, there should be no difference between the two referencing methods and either of them should work fine in any browser or mail agent. In practice, however, some agents fail to fetch resources by file name. If your browser or mail agent refuses to load resources included in an MTHML document (doesn't show images or doesn't load CSS styles), try exporting the document with CID URLs.

**Returns:**
boolean - The corresponding  boolean  value.
### setExportCidUrlsForMhtmlResources(boolean value) {#setExportCidUrlsForMhtmlResources-boolean-}
```
public void setExportCidUrlsForMhtmlResources(boolean value)
```


Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is  false .

This option affects only documents being saved to MHTML.

By default, resources in MHTML documents are referenced by file name (for example, "image.png"), which are matched against "Content-Location" headers of MIME parts.

This option enables an alternative method, where references to resource files are written as CID (Content-ID) URLs (for example, "cid:image.png") and are matched against "Content-ID" headers.

In theory, there should be no difference between the two referencing methods and either of them should work fine in any browser or mail agent. In practice, however, some agents fail to fetch resources by file name. If your browser or mail agent refuses to load resources included in an MTHML document (doesn't show images or doesn't load CSS styles), try exporting the document with CID URLs.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getResolveFontNames() {#getResolveFontNames--}
```
public boolean getResolveFontNames()
```


Specifies whether font family names used in the document are resolved and substituted according to [Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) when being written into HTML-based formats.

By default, this option is set to  false  and font family names are written to HTML as specified in source documents. That is, [Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) are ignored and no resolution or substitution of font family names is performed.

If this option is set to  true , Aspose.Words uses [Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) to resolve each font family name specified in a source document into the name of an available font family, performing font substitution as required.

**Returns:**
boolean - The corresponding  boolean  value.
### setResolveFontNames(boolean value) {#setResolveFontNames-boolean-}
```
public void setResolveFontNames(boolean value)
```


Specifies whether font family names used in the document are resolved and substituted according to [Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) when being written into HTML-based formats.

By default, this option is set to  false  and font family names are written to HTML as specified in source documents. That is, [Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) are ignored and no resolution or substitution of font family names is performed.

If this option is set to  true , Aspose.Words uses [Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) to resolve each font family name specified in a source document into the name of an available font family, performing font substitution as required.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

