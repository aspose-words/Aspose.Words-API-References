---
title: PdfSaveOptions
second_title: Aspose.Words for Java API Reference
description: Can be used to specify additional options when saving a document into the  format.
type: docs
weight: 461
url: /java/com.aspose.words/pdfsaveoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class PdfSaveOptions extends FixedPageSaveOptions implements Cloneable
```

Can be used to specify additional options when saving a document into the [SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF) format.

To learn more, visit the **Specify Save Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [PdfSaveOptions()](#PdfSaveOptions--) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF) format. |
## Methods

| Method | Description |
| --- | --- |
| [getSaveFormat()](#getSaveFormat--) | Specifies the format in which the document will be saved if this save options object is used. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Specifies the format in which the document will be saved if this save options object is used. |
| [getOutlineOptions()](#getOutlineOptions--) | Allows to specify outline options. |
| [getTextCompression()](#getTextCompression--) | Specifies compression type to be used for all textual content in the document. |
| [setTextCompression(int value)](#setTextCompression-int-) | Specifies compression type to be used for all textual content in the document. |
| [getJpegQuality()](#getJpegQuality--) | Gets a value determining the quality of the JPEG images inside PDF document. |
| [setJpegQuality(int value)](#setJpegQuality-int-) | Sets a value determining the quality of the JPEG images inside PDF document. |
| [getPreserveFormFields()](#getPreserveFormFields--) | Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. |
| [setPreserveFormFields(boolean value)](#setPreserveFormFields-boolean-) | Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. |
| [getCreateNoteHyperlinks()](#getCreateNoteHyperlinks--) | Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. |
| [setCreateNoteHyperlinks(boolean value)](#setCreateNoteHyperlinks-boolean-) | Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. |
| [getEncryptionDetails()](#getEncryptionDetails--) | Gets the details for encrypting the output PDF document. |
| [setEncryptionDetails(PdfEncryptionDetails value)](#setEncryptionDetails-com.aspose.words.PdfEncryptionDetails-) | Sets the details for encrypting the output PDF document. |
| [getDigitalSignatureDetails()](#getDigitalSignatureDetails--) | Gets the details for signing the output PDF document. |
| [setDigitalSignatureDetails(PdfDigitalSignatureDetails value)](#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails-) | Sets the details for signing the output PDF document. |
| [deepClone()](#deepClone--) | Creates a deep clone of this object. |
| [getEmbedFullFonts()](#getEmbedFullFonts--) | Controls how fonts are embedded into the resulting PDF documents. |
| [setEmbedFullFonts(boolean value)](#setEmbedFullFonts-boolean-) | Controls how fonts are embedded into the resulting PDF documents. |
| [getFontEmbeddingMode()](#getFontEmbeddingMode--) | Specifies the font embedding mode. |
| [setFontEmbeddingMode(int value)](#setFontEmbeddingMode-int-) | Specifies the font embedding mode. |
| [getUseCoreFonts()](#getUseCoreFonts--) | Gets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |
| [setUseCoreFonts(boolean value)](#setUseCoreFonts-boolean-) | Sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |
| [getCustomPropertiesExport()](#getCustomPropertiesExport--) | Gets a value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) are exported to PDF file. |
| [setCustomPropertiesExport(int value)](#setCustomPropertiesExport-int-) | Sets a value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) are exported to PDF file. |
| [getZoomBehavior()](#getZoomBehavior--) | Gets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. |
| [setZoomBehavior(int value)](#setZoomBehavior-int-) | Sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. |
| [getZoomFactor()](#getZoomFactor--) | Gets a value determining zoom factor (in percentages) for a document. |
| [setZoomFactor(int value)](#setZoomFactor-int-) | Sets a value determining zoom factor (in percentages) for a document. |
| [getImageCompression()](#getImageCompression--) | Specifies compression type to be used for all images in the document. |
| [setImageCompression(int value)](#setImageCompression-int-) | Specifies compression type to be used for all images in the document. |
| [getOpenHyperlinksInNewWindow()](#getOpenHyperlinksInNewWindow--) | Gets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |
| [setOpenHyperlinksInNewWindow(boolean value)](#setOpenHyperlinksInNewWindow-boolean-) | Sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |
| [getExportDocumentStructure()](#getExportDocumentStructure--) | Gets a value determining whether or not to export document structure. |
| [setExportDocumentStructure(boolean value)](#setExportDocumentStructure-boolean-) | Sets a value determining whether or not to export document structure. |
| [getExportLanguageToSpanTag()](#getExportLanguageToSpanTag--) | Gets a value determining whether or not to create a "Span" tag in the document structure to export the text language. |
| [setExportLanguageToSpanTag(boolean value)](#setExportLanguageToSpanTag-boolean-) | Sets a value determining whether or not to create a "Span" tag in the document structure to export the text language. |
| [getUseBookFoldPrintingSettings()](#getUseBookFoldPrintingSettings--) | Gets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |
| [setUseBookFoldPrintingSettings(boolean value)](#setUseBookFoldPrintingSettings-boolean-) | Sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |
| [getDownsampleOptions()](#getDownsampleOptions--) | Allows to specify downsample options. |
| [setDownsampleOptions(DownsampleOptions value)](#setDownsampleOptions-com.aspose.words.DownsampleOptions-) | Allows to specify downsample options. |
| [getPageMode()](#getPageMode--) | Specifies how the PDF document should be displayed when opened in the PDF reader. |
| [setPageMode(int value)](#setPageMode-int-) | Specifies how the PDF document should be displayed when opened in the PDF reader. |
| [getImageColorSpaceExportMode()](#getImageColorSpaceExportMode--) | Specifies how the color space will be selected for the images in PDF document. |
| [setImageColorSpaceExportMode(int value)](#setImageColorSpaceExportMode-int-) | Specifies how the color space will be selected for the images in PDF document. |
| [getPreblendImages()](#getPreblendImages--) | Gets a value determining whether or not to preblend transparent images with black background color. |
| [setPreblendImages(boolean value)](#setPreblendImages-boolean-) | Sets a value determining whether or not to preblend transparent images with black background color. |
| [getDisplayDocTitle()](#getDisplayDocTitle--) | A flag specifying whether the window\\u2019s title bar should display the document title taken from the Title entry of the document information dictionary. |
| [setDisplayDocTitle(boolean value)](#setDisplayDocTitle-boolean-) | A flag specifying whether the window\\u2019s title bar should display the document title taken from the Title entry of the document information dictionary. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | Gets a value determining how DrawingML effects are rendered. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | Sets a value determining how DrawingML effects are rendered. |
| [getHeaderFooterBookmarksExportMode()](#getHeaderFooterBookmarksExportMode--) | Determines how bookmarks in headers/footers are exported. |
| [setHeaderFooterBookmarksExportMode(int value)](#setHeaderFooterBookmarksExportMode-int-) | Determines how bookmarks in headers/footers are exported. |
| [getAdditionalTextPositioning()](#getAdditionalTextPositioning--) | A flag specifying whether to write additional text positioning operators or not. |
| [setAdditionalTextPositioning(boolean value)](#setAdditionalTextPositioning-boolean-) | A flag specifying whether to write additional text positioning operators or not. |
| [getInterpolateImages()](#getInterpolateImages--) | A flag indicating whether image interpolation shall be performed by a conforming reader. |
| [setInterpolateImages(boolean value)](#setInterpolateImages-boolean-) | A flag indicating whether image interpolation shall be performed by a conforming reader. |
| [getCompliance()](#getCompliance--) | Specifies the PDF standards compliance level for output documents. |
| [setCompliance(int value)](#setCompliance-int-) | Specifies the PDF standards compliance level for output documents. |
| [getCacheHeaderFooterShapes()](#getCacheHeaderFooterShapes--) | Gets a value determining whether or not to cache shapes placed in header and footer of document. |
| [setCacheHeaderFooterShapes(boolean value)](#setCacheHeaderFooterShapes-boolean-) | Sets a value determining whether or not to cache shapes placed in header and footer of document. |
### PdfSaveOptions() {#PdfSaveOptions--}
```
public PdfSaveOptions()
```


Initializes a new instance of this class that can be used to save a document in the [SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF) format.

### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF).

**Returns:**
int - The corresponding  int  value. The returned value is one of [SaveFormat](../../com.aspose.words/saveformat) constants.
### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SaveFormat](../../com.aspose.words/saveformat) constants. |

### getOutlineOptions() {#getOutlineOptions--}
```
public OutlineOptions getOutlineOptions()
```


Allows to specify outline options.

Outlines can be created from headings and bookmarks.

For headings outline level is determined by the heading level.

It is possible to set the max heading level to be included into outlines or disable heading outlines at all.

For bookmarks outline level may be set in options as a default value for all bookmarks or as individual values for particular bookmarks.

Also, outlines can be exported to XPS format by using the same [getOutlineOptions()](../../com.aspose.words/pdfsaveoptions\#getOutlineOptions--) class.

**Returns:**
[OutlineOptions](../../com.aspose.words/outlineoptions) - The corresponding [OutlineOptions](../../com.aspose.words/outlineoptions) value.
### getTextCompression() {#getTextCompression--}
```
public int getTextCompression()
```


Specifies compression type to be used for all textual content in the document.

Default is [PdfTextCompression.FLATE](../../com.aspose.words/pdftextcompression\#FLATE).

Significantly increases output size when saving a document without compression.

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfTextCompression](../../com.aspose.words/pdftextcompression) constants.
### setTextCompression(int value) {#setTextCompression-int-}
```
public void setTextCompression(int value)
```


Specifies compression type to be used for all textual content in the document.

Default is [PdfTextCompression.FLATE](../../com.aspose.words/pdftextcompression\#FLATE).

Significantly increases output size when saving a document without compression.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfTextCompression](../../com.aspose.words/pdftextcompression) constants. |

### getJpegQuality() {#getJpegQuality--}
```
public int getJpegQuality()
```


Gets a value determining the quality of the JPEG images inside PDF document.

The default value is 100.

This property is used in conjunction with the [getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-) option.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in PDF format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression. If quality is 100 and source image is JPEG, it means no compression - original bytes will be saved.

**Returns:**
int - A value determining the quality of the JPEG images inside PDF document.
### setJpegQuality(int value) {#setJpegQuality-int-}
```
public void setJpegQuality(int value)
```


Sets a value determining the quality of the JPEG images inside PDF document.

The default value is 100.

This property is used in conjunction with the [getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-) option.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in PDF format. The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100 means best quality but minimum compression. If quality is 100 and source image is JPEG, it means no compression - original bytes will be saved.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining the quality of the JPEG images inside PDF document. |

### getPreserveFormFields() {#getPreserveFormFields--}
```
public boolean getPreserveFormFields()
```


Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is  false .

Microsoft Word form fields include text input, drop down and check box controls.

When set to  false , these fields will be exported as text to PDF. When set to  true , these fields will be exported as PDF form fields.

When exporting form fields to PDF as form fields, some formatting loss might occur because PDF form fields do not support all features of Microsoft Word form fields.

Also, the output size depends on the content size because editable forms in Microsoft Word are inline objects.

Editable forms are prohibited by PDF/A compliance.  false  value will be used automatically when saving to PDF/A.

Form fields are not supported when saving to PDF/UA.  false  value will be used automatically.

**Returns:**
boolean - The corresponding  boolean  value.
### setPreserveFormFields(boolean value) {#setPreserveFormFields-boolean-}
```
public void setPreserveFormFields(boolean value)
```


Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is  false .

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

### getCreateNoteHyperlinks() {#getCreateNoteHyperlinks--}
```
public boolean getCreateNoteHyperlinks()
```


Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### setCreateNoteHyperlinks(boolean value) {#setCreateNoteHyperlinks-boolean-}
```
public void setCreateNoteHyperlinks(boolean value)
```


Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getEncryptionDetails() {#getEncryptionDetails--}
```
public PdfEncryptionDetails getEncryptionDetails()
```


Gets the details for encrypting the output PDF document.

The default value is null and the output document will not be encrypted. When this property is set to a valid [PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails) object, then the output PDF document will be encrypted.

AES-128 encryption algorithm is used when saving to PDF 1.7 based compliance (including PDF/UA-1). AES-256 encryption algorithm is used when saving to PDF 2.0 based compliance.

Encryption is prohibited by PDF/A compliance. This option will be ignored when saving to PDF/A.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0.

**Returns:**
[PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails) - The details for encrypting the output PDF document.
### setEncryptionDetails(PdfEncryptionDetails value) {#setEncryptionDetails-com.aspose.words.PdfEncryptionDetails-}
```
public void setEncryptionDetails(PdfEncryptionDetails value)
```


Sets the details for encrypting the output PDF document.

The default value is null and the output document will not be encrypted. When this property is set to a valid [PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails) object, then the output PDF document will be encrypted.

AES-128 encryption algorithm is used when saving to PDF 1.7 based compliance (including PDF/UA-1). AES-256 encryption algorithm is used when saving to PDF 2.0 based compliance.

Encryption is prohibited by PDF/A compliance. This option will be ignored when saving to PDF/A.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY) permission is required by PDF/UA compliance if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY) permission is deprecated in PDF 2.0 format. This permission will be ignored when saving to PDF 2.0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails) | The details for encrypting the output PDF document. |

### getDigitalSignatureDetails() {#getDigitalSignatureDetails--}
```
public PdfDigitalSignatureDetails getDigitalSignatureDetails()
```


Gets the details for signing the output PDF document.

The default value is null and the output document will not be signed. When this property is set to a valid [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) object, then the output PDF document will be digitally signed.

**Returns:**
[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) - The details for signing the output PDF document.
### setDigitalSignatureDetails(PdfDigitalSignatureDetails value) {#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails-}
```
public void setDigitalSignatureDetails(PdfDigitalSignatureDetails value)
```


Sets the details for signing the output PDF document.

The default value is null and the output document will not be signed. When this property is set to a valid [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) object, then the output PDF document will be digitally signed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) | The details for signing the output PDF document. |

### deepClone() {#deepClone--}
```
public PdfSaveOptions deepClone()
```


Creates a deep clone of this object.

**Returns:**
[PdfSaveOptions](../../com.aspose.words/pdfsaveoptions)
### getEmbedFullFonts() {#getEmbedFullFonts--}
```
public boolean getEmbedFullFonts()
```


Controls how fonts are embedded into the resulting PDF documents.

The default value is  false , which means the fonts are subsetted before embedding. Subsetting is useful if you want to keep the output file size smaller. Subsetting removes all unused glyphs from a font.

When this value is set to  true , a complete font file is embedded into PDF without subsetting. This will result in larger output files, but can be a useful option when you want to edit the resulting PDF later (e.g. add more text).

Some fonts are large (several megabytes) and embedding them without subsetting will result in large output documents.

**Returns:**
boolean - The corresponding  boolean  value.
### setEmbedFullFonts(boolean value) {#setEmbedFullFonts-boolean-}
```
public void setEmbedFullFonts(boolean value)
```


Controls how fonts are embedded into the resulting PDF documents.

The default value is  false , which means the fonts are subsetted before embedding. Subsetting is useful if you want to keep the output file size smaller. Subsetting removes all unused glyphs from a font.

When this value is set to  true , a complete font file is embedded into PDF without subsetting. This will result in larger output files, but can be a useful option when you want to edit the resulting PDF later (e.g. add more text).

Some fonts are large (several megabytes) and embedding them without subsetting will result in large output documents.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getFontEmbeddingMode() {#getFontEmbeddingMode--}
```
public int getFontEmbeddingMode()
```


Specifies the font embedding mode.

The default value is [PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL).

This setting works only for the text in ANSI (Windows-1252) encoding. If the document contains non-ANSI text then corresponding fonts will be embedded regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded. [PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL) value will be used automatically when saving to PDF/A and PDF/UA.

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfFontEmbeddingMode](../../com.aspose.words/pdffontembeddingmode) constants.
### setFontEmbeddingMode(int value) {#setFontEmbeddingMode-int-}
```
public void setFontEmbeddingMode(int value)
```


Specifies the font embedding mode.

The default value is [PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL).

This setting works only for the text in ANSI (Windows-1252) encoding. If the document contains non-ANSI text then corresponding fonts will be embedded regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded. [PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL) value will be used automatically when saving to PDF/A and PDF/UA.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfFontEmbeddingMode](../../com.aspose.words/pdffontembeddingmode) constants. |

### getUseCoreFonts() {#getUseCoreFonts--}
```
public boolean getUseCoreFonts()
```


Gets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts.

The default value is  false . When this value is set to  true  Arial, Times New Roman, Courier New and Symbol fonts are replaced in PDF document with corresponding core Type 1 font.

Core PDF fonts, or their font metrics and suitable substitution fonts, are required to be available to any PDF viewer application.

This setting works only for the text in ANSI (Windows-1252) encoding. Non-ANSI text will be written with embedded TrueType font regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded.  false  value will be used automatically when saving to PDF/A and PDF/UA.

Core fonts are not supported when saving to PDF 2.0 format.  false  value will be used automatically when saving to PDF 2.0.

This option has a higher priority then [getFontEmbeddingMode()](../../com.aspose.words/pdfsaveoptions\#getFontEmbeddingMode--) / [setFontEmbeddingMode(int)](../../com.aspose.words/pdfsaveoptions\#setFontEmbeddingMode-int-) option.

**Returns:**
boolean - A value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts.
### setUseCoreFonts(boolean value) {#setUseCoreFonts-boolean-}
```
public void setUseCoreFonts(boolean value)
```


Sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts.

The default value is  false . When this value is set to  true  Arial, Times New Roman, Courier New and Symbol fonts are replaced in PDF document with corresponding core Type 1 font.

Core PDF fonts, or their font metrics and suitable substitution fonts, are required to be available to any PDF viewer application.

This setting works only for the text in ANSI (Windows-1252) encoding. Non-ANSI text will be written with embedded TrueType font regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded.  false  value will be used automatically when saving to PDF/A and PDF/UA.

Core fonts are not supported when saving to PDF 2.0 format.  false  value will be used automatically when saving to PDF 2.0.

This option has a higher priority then [getFontEmbeddingMode()](../../com.aspose.words/pdfsaveoptions\#getFontEmbeddingMode--) / [setFontEmbeddingMode(int)](../../com.aspose.words/pdfsaveoptions\#setFontEmbeddingMode-int-) option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |

### getCustomPropertiesExport() {#getCustomPropertiesExport--}
```
public int getCustomPropertiesExport()
```


Gets a value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) are exported to PDF file.

Default value is [PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE).

[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA) value is not supported when saving to PDF/A. [PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD) will be used instead for PDF/A-1 and PDF/A-2 and [PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE) for PDF/A-4.

[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD) value is not supported when saving to PDF 2.0. [PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA) will be used instead.

**Returns:**
int - A value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) are exported to PDF file. The returned value is one of [PdfCustomPropertiesExport](../../com.aspose.words/pdfcustompropertiesexport) constants.
### setCustomPropertiesExport(int value) {#setCustomPropertiesExport-int-}
```
public void setCustomPropertiesExport(int value)
```


Sets a value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) are exported to PDF file.

Default value is [PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE).

[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA) value is not supported when saving to PDF/A. [PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD) will be used instead for PDF/A-1 and PDF/A-2 and [PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE) for PDF/A-4.

[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD) value is not supported when saving to PDF 2.0. [PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA) will be used instead.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) are exported to PDF file. The value must be one of [PdfCustomPropertiesExport](../../com.aspose.words/pdfcustompropertiesexport) constants. |

### getZoomBehavior() {#getZoomBehavior--}
```
public int getZoomBehavior()
```


Gets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. The default value is [PdfZoomBehavior.NONE](../../com.aspose.words/pdfzoombehavior\#NONE), i.e. no fit is applied.

**Returns:**
int - A value determining what type of zoom should be applied when a document is opened with a PDF viewer. The returned value is one of [PdfZoomBehavior](../../com.aspose.words/pdfzoombehavior) constants.
### setZoomBehavior(int value) {#setZoomBehavior-int-}
```
public void setZoomBehavior(int value)
```


Sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. The default value is [PdfZoomBehavior.NONE](../../com.aspose.words/pdfzoombehavior\#NONE), i.e. no fit is applied.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining what type of zoom should be applied when a document is opened with a PDF viewer. The value must be one of [PdfZoomBehavior](../../com.aspose.words/pdfzoombehavior) constants. |

### getZoomFactor() {#getZoomFactor--}
```
public int getZoomFactor()
```


Gets a value determining zoom factor (in percentages) for a document. This value is used only if [getZoomBehavior()](../../com.aspose.words/pdfsaveoptions\#getZoomBehavior--) / [setZoomBehavior(int)](../../com.aspose.words/pdfsaveoptions\#setZoomBehavior-int-) is set to [PdfZoomBehavior.ZOOM\_FACTOR](../../com.aspose.words/pdfzoombehavior\#ZOOM-FACTOR).

**Returns:**
int - A value determining zoom factor (in percentages) for a document.
### setZoomFactor(int value) {#setZoomFactor-int-}
```
public void setZoomFactor(int value)
```


Sets a value determining zoom factor (in percentages) for a document. This value is used only if [getZoomBehavior()](../../com.aspose.words/pdfsaveoptions\#getZoomBehavior--) / [setZoomBehavior(int)](../../com.aspose.words/pdfsaveoptions\#setZoomBehavior-int-) is set to [PdfZoomBehavior.ZOOM\_FACTOR](../../com.aspose.words/pdfzoombehavior\#ZOOM-FACTOR).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining zoom factor (in percentages) for a document. |

### getImageCompression() {#getImageCompression--}
```
public int getImageCompression()
```


Specifies compression type to be used for all images in the document.

Default is [PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO).

Using [PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG) lets you control the quality of images in the output document through the [getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-) property.

Using [PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG) provides the fastest conversion speed when compared to the performance of other compression types, but in this case, there is lossy JPEG compression.

Using [PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO) lets to control the quality of Jpeg in the output document through the [getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-) property, but for other formats, raw pixel data is extracted and saved with Flate compression. This case is slower than Jpeg conversion but lossless.

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfImageCompression](../../com.aspose.words/pdfimagecompression) constants.
### setImageCompression(int value) {#setImageCompression-int-}
```
public void setImageCompression(int value)
```


Specifies compression type to be used for all images in the document.

Default is [PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO).

Using [PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG) lets you control the quality of images in the output document through the [getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-) property.

Using [PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG) provides the fastest conversion speed when compared to the performance of other compression types, but in this case, there is lossy JPEG compression.

Using [PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO) lets to control the quality of Jpeg in the output document through the [getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-) property, but for other formats, raw pixel data is extracted and saved with Flate compression. This case is slower than Jpeg conversion but lossless.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfImageCompression](../../com.aspose.words/pdfimagecompression) constants. |

### getOpenHyperlinksInNewWindow() {#getOpenHyperlinksInNewWindow--}
```
public boolean getOpenHyperlinksInNewWindow()
```


Gets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser.

The default value is  false . When this value is set to  true  hyperlinks are saved using JavaScript code. JavaScript code is  app.launchURL("URL", true); , where  URL  is a hyperlink.

Note that if this option is set to  true  hyperlinks can't work in some PDF readers e.g. Chrome, Firefox.

JavaScript actions are prohibited by PDF/A-1 and PDF/A-2 compliance.  false  will be used automatically when saving to PDF/A-1 and PDF/A-2.

**Returns:**
boolean - A value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser.
### setOpenHyperlinksInNewWindow(boolean value) {#setOpenHyperlinksInNewWindow-boolean-}
```
public void setOpenHyperlinksInNewWindow(boolean value)
```


Sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser.

The default value is  false . When this value is set to  true  hyperlinks are saved using JavaScript code. JavaScript code is  app.launchURL("URL", true); , where  URL  is a hyperlink.

Note that if this option is set to  true  hyperlinks can't work in some PDF readers e.g. Chrome, Firefox.

JavaScript actions are prohibited by PDF/A-1 and PDF/A-2 compliance.  false  will be used automatically when saving to PDF/A-1 and PDF/A-2.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |

### getExportDocumentStructure() {#getExportDocumentStructure--}
```
public boolean getExportDocumentStructure()
```


Gets a value determining whether or not to export document structure.

This value is ignored when saving to PDF/A-1a, PDF/A-2a and PDF/UA-1 because document structure is required for this compliance.

Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

**Returns:**
boolean - A value determining whether or not to export document structure.
### setExportDocumentStructure(boolean value) {#setExportDocumentStructure-boolean-}
```
public void setExportDocumentStructure(boolean value)
```


Sets a value determining whether or not to export document structure.

This value is ignored when saving to PDF/A-1a, PDF/A-2a and PDF/UA-1 because document structure is required for this compliance.

Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to export document structure. |

### getExportLanguageToSpanTag() {#getExportLanguageToSpanTag--}
```
public boolean getExportLanguageToSpanTag()
```


Gets a value determining whether or not to create a "Span" tag in the document structure to export the text language.

Default value is  false  and "Lang" attribute is attached to a marked-content sequence in a page content stream.

When the value is  true  "Span" tag is created for the text with non-default language and "Lang" attribute is attached to this tag.

This value is ignored when [getExportDocumentStructure()](../../com.aspose.words/pdfsaveoptions\#getExportDocumentStructure--) / [setExportDocumentStructure(boolean)](../../com.aspose.words/pdfsaveoptions\#setExportDocumentStructure-boolean-) is  false .

**Returns:**
boolean - A value determining whether or not to create a "Span" tag in the document structure to export the text language.
### setExportLanguageToSpanTag(boolean value) {#setExportLanguageToSpanTag-boolean-}
```
public void setExportLanguageToSpanTag(boolean value)
```


Sets a value determining whether or not to create a "Span" tag in the document structure to export the text language.

Default value is  false  and "Lang" attribute is attached to a marked-content sequence in a page content stream.

When the value is  true  "Span" tag is created for the text with non-default language and "Lang" attribute is attached to this tag.

This value is ignored when [getExportDocumentStructure()](../../com.aspose.words/pdfsaveoptions\#getExportDocumentStructure--) / [setExportDocumentStructure(boolean)](../../com.aspose.words/pdfsaveoptions\#setExportDocumentStructure-boolean-) is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to create a "Span" tag in the document structure to export the text language. |

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

### getDownsampleOptions() {#getDownsampleOptions--}
```
public DownsampleOptions getDownsampleOptions()
```


Allows to specify downsample options.

**Returns:**
[DownsampleOptions](../../com.aspose.words/downsampleoptions) - The corresponding [DownsampleOptions](../../com.aspose.words/downsampleoptions) value.
### setDownsampleOptions(DownsampleOptions value) {#setDownsampleOptions-com.aspose.words.DownsampleOptions-}
```
public void setDownsampleOptions(DownsampleOptions value)
```


Allows to specify downsample options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [DownsampleOptions](../../com.aspose.words/downsampleoptions) | The corresponding [DownsampleOptions](../../com.aspose.words/downsampleoptions) value. |

### getPageMode() {#getPageMode--}
```
public int getPageMode()
```


Specifies how the PDF document should be displayed when opened in the PDF reader. The default value is [PdfPageMode.USE\_OUTLINES](../../com.aspose.words/pdfpagemode\#USE-OUTLINES).

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfPageMode](../../com.aspose.words/pdfpagemode) constants.
### setPageMode(int value) {#setPageMode-int-}
```
public void setPageMode(int value)
```


Specifies how the PDF document should be displayed when opened in the PDF reader. The default value is [PdfPageMode.USE\_OUTLINES](../../com.aspose.words/pdfpagemode\#USE-OUTLINES).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfPageMode](../../com.aspose.words/pdfpagemode) constants. |

### getImageColorSpaceExportMode() {#getImageColorSpaceExportMode--}
```
public int getImageColorSpaceExportMode()
```


Specifies how the color space will be selected for the images in PDF document.

The default value is [PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO).

If [PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK) value is specified, [getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-) option is ignored and Flate compression is used for all images in the document.

[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK) value is not supported when saving to PDF/A. [PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO) value will be used instead.

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfImageColorSpaceExportMode](../../com.aspose.words/pdfimagecolorspaceexportmode) constants.
### setImageColorSpaceExportMode(int value) {#setImageColorSpaceExportMode-int-}
```
public void setImageColorSpaceExportMode(int value)
```


Specifies how the color space will be selected for the images in PDF document.

The default value is [PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO).

If [PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK) value is specified, [getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-) option is ignored and Flate compression is used for all images in the document.

[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK) value is not supported when saving to PDF/A. [PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO) value will be used instead.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfImageColorSpaceExportMode](../../com.aspose.words/pdfimagecolorspaceexportmode) constants. |

### getPreblendImages() {#getPreblendImages--}
```
public boolean getPreblendImages()
```


Gets a value determining whether or not to preblend transparent images with black background color.

Preblending images may improve PDF document visual appearance in Adobe Reader and remove anti-aliasing artifacts.

In order to properly display preblended images, PDF viewer application must support /Matte entry in soft-mask image dictionary. Also preblending images may decrease PDF rendering performance.

The default value is  false .

**Returns:**
boolean - A value determining whether or not to preblend transparent images with black background color.
### setPreblendImages(boolean value) {#setPreblendImages-boolean-}
```
public void setPreblendImages(boolean value)
```


Sets a value determining whether or not to preblend transparent images with black background color.

Preblending images may improve PDF document visual appearance in Adobe Reader and remove anti-aliasing artifacts.

In order to properly display preblended images, PDF viewer application must support /Matte entry in soft-mask image dictionary. Also preblending images may decrease PDF rendering performance.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to preblend transparent images with black background color. |

### getDisplayDocTitle() {#getDisplayDocTitle--}
```
public boolean getDisplayDocTitle()
```


A flag specifying whether the window\\u2019s title bar should display the document title taken from the Title entry of the document information dictionary.

If  false , the title bar should instead display the name of the PDF file containing the document.

This flag is required by PDF/UA compliance.  true  value will be used automatically when saving to PDF/UA.

The default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### setDisplayDocTitle(boolean value) {#setDisplayDocTitle-boolean-}
```
public void setDisplayDocTitle(boolean value)
```


A flag specifying whether the window\\u2019s title bar should display the document title taken from the Title entry of the document information dictionary.

If  false , the title bar should instead display the name of the PDF file containing the document.

This flag is required by PDF/UA compliance.  true  value will be used automatically when saving to PDF/UA.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode--}
```
public int getDmlEffectsRenderingMode()
```


Gets a value determining how DrawingML effects are rendered. The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

If [getCompliance()](../../com.aspose.words/pdfsaveoptions\#getCompliance--) / [setCompliance(int)](../../com.aspose.words/pdfsaveoptions\#setCompliance-int-) is set to [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A) or [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B), property always returns [DmlEffectsRenderingMode.NONE](../../com.aspose.words/dmleffectsrenderingmode\#NONE).

**Returns:**
int - A value determining how DrawingML effects are rendered. The returned value is one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) constants.
### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int-}
```
public void setDmlEffectsRenderingMode(int value)
```


Sets a value determining how DrawingML effects are rendered. The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

This property is used when the document is exported to fixed page formats.

If [getCompliance()](../../com.aspose.words/pdfsaveoptions\#getCompliance--) / [setCompliance(int)](../../com.aspose.words/pdfsaveoptions\#setCompliance-int-) is set to [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A) or [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B), property always returns [DmlEffectsRenderingMode.NONE](../../com.aspose.words/dmleffectsrenderingmode\#NONE).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value determining how DrawingML effects are rendered. The value must be one of [DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) constants. |

### getHeaderFooterBookmarksExportMode() {#getHeaderFooterBookmarksExportMode--}
```
public int getHeaderFooterBookmarksExportMode()
```


Determines how bookmarks in headers/footers are exported.

The default value is [HeaderFooterBookmarksExportMode.ALL](../../com.aspose.words/headerfooterbookmarksexportmode\#ALL).

This property is used in conjunction with the [getOutlineOptions()](../../com.aspose.words/pdfsaveoptions\#getOutlineOptions--) option.

**Returns:**
int - The corresponding  int  value. The returned value is one of [HeaderFooterBookmarksExportMode](../../com.aspose.words/headerfooterbookmarksexportmode) constants.
### setHeaderFooterBookmarksExportMode(int value) {#setHeaderFooterBookmarksExportMode-int-}
```
public void setHeaderFooterBookmarksExportMode(int value)
```


Determines how bookmarks in headers/footers are exported.

The default value is [HeaderFooterBookmarksExportMode.ALL](../../com.aspose.words/headerfooterbookmarksexportmode\#ALL).

This property is used in conjunction with the [getOutlineOptions()](../../com.aspose.words/pdfsaveoptions\#getOutlineOptions--) option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [HeaderFooterBookmarksExportMode](../../com.aspose.words/headerfooterbookmarksexportmode) constants. |

### getAdditionalTextPositioning() {#getAdditionalTextPositioning--}
```
public boolean getAdditionalTextPositioning()
```


A flag specifying whether to write additional text positioning operators or not.

If  true , additional text positioning operators are written to the output PDF. This may help to overcome issues with inaccurate text positioning with some printers. The downside is the increased PDF document size.

The default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### setAdditionalTextPositioning(boolean value) {#setAdditionalTextPositioning-boolean-}
```
public void setAdditionalTextPositioning(boolean value)
```


A flag specifying whether to write additional text positioning operators or not.

If  true , additional text positioning operators are written to the output PDF. This may help to overcome issues with inaccurate text positioning with some printers. The downside is the increased PDF document size.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getInterpolateImages() {#getInterpolateImages--}
```
public boolean getInterpolateImages()
```


A flag indicating whether image interpolation shall be performed by a conforming reader. When  false  is specified, the flag is not written to the output document and the default behaviour of reader is used instead.

When the resolution of a source image is significantly lower than that of the output device, each source sample covers many device pixels. As a result, images can appear jaggy or blocky. These visual artifacts can be reduced by applying an image interpolation algorithm during rendering. Instead of painting all pixels covered by a source sample with the same color, image interpolation attempts to produce a smooth transition between adjacent sample values.

A conforming Reader may choose to not implement this feature of PDF, or may use any specific implementation of interpolation that it wishes.

The default value is  false .

Interpolation flag is prohibited by PDF/A compliance.  false  value will be used automatically when saving to PDF/A.

**Returns:**
boolean - The corresponding  boolean  value.
### setInterpolateImages(boolean value) {#setInterpolateImages-boolean-}
```
public void setInterpolateImages(boolean value)
```


A flag indicating whether image interpolation shall be performed by a conforming reader. When  false  is specified, the flag is not written to the output document and the default behaviour of reader is used instead.

When the resolution of a source image is significantly lower than that of the output device, each source sample covers many device pixels. As a result, images can appear jaggy or blocky. These visual artifacts can be reduced by applying an image interpolation algorithm during rendering. Instead of painting all pixels covered by a source sample with the same color, image interpolation attempts to produce a smooth transition between adjacent sample values.

A conforming Reader may choose to not implement this feature of PDF, or may use any specific implementation of interpolation that it wishes.

The default value is  false .

Interpolation flag is prohibited by PDF/A compliance.  false  value will be used automatically when saving to PDF/A.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getCompliance() {#getCompliance--}
```
public int getCompliance()
```


Specifies the PDF standards compliance level for output documents.

Default is [PdfCompliance.PDF\_17](../../com.aspose.words/pdfcompliance\#PDF-17).

**Returns:**
int - The corresponding  int  value. The returned value is one of [PdfCompliance](../../com.aspose.words/pdfcompliance) constants.
### setCompliance(int value) {#setCompliance-int-}
```
public void setCompliance(int value)
```


Specifies the PDF standards compliance level for output documents.

Default is [PdfCompliance.PDF\_17](../../com.aspose.words/pdfcompliance\#PDF-17).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [PdfCompliance](../../com.aspose.words/pdfcompliance) constants. |

### getCacheHeaderFooterShapes() {#getCacheHeaderFooterShapes--}
```
public boolean getCacheHeaderFooterShapes()
```


Gets a value determining whether or not to cache shapes placed in header and footer of document.

Default value is  false  and shapes are not cached.

When the value is  true  shapes graphics are written to the PDF document as an xObject.

Some shapes are not supported for caching(shapes with fields, bookmarks, HRefs).

**Returns:**
boolean - A value determining whether or not to cache shapes placed in header and footer of document.
### setCacheHeaderFooterShapes(boolean value) {#setCacheHeaderFooterShapes-boolean-}
```
public void setCacheHeaderFooterShapes(boolean value)
```


Sets a value determining whether or not to cache shapes placed in header and footer of document.

Default value is  false  and shapes are not cached.

When the value is  true  shapes graphics are written to the PDF document as an xObject.

Some shapes are not supported for caching(shapes with fields, bookmarks, HRefs).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value determining whether or not to cache shapes placed in header and footer of document. |

