---
title: PdfSaveOptions
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 5150
url: /net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Can be used to specify additional options when saving a document into the Pdf format.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Public Members

| name | description |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions)() | Initializes a new instance of this class that can be used to save a document in the Pdf format. |
| [AdditionalTextPositioning](additionaltextpositioning) { get; set; } | A flag specifying whether to write additional text positioning operators or not. |
| [Compliance](compliance) { get; set; } | Specifies the PDF standards compliance level for output documents. |
| [CreateNoteHyperlinks](createnotehyperlinks) { get; set; } | Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is `false`. |
| [CustomPropertiesExport](custompropertiesexport) { get; set; } | Gets or sets a value determining the way [`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties) are exported to PDF file. |
| [DigitalSignatureDetails](digitalsignaturedetails) { get; set; } | Gets or sets the details for signing the output PDF document. |
| [DisplayDocTitle](displaydoctitle) { get; set; } | A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary. |
| override [DmlEffectsRenderingMode](dmleffectsrenderingmode) { get; set; } | Gets or sets a value determining how DrawingML effects are rendered. |
| [DownsampleOptions](downsampleoptions) { get; set; } | Allows to specify downsample options. |
| [EmbedFullFonts](embedfullfonts) { get; set; } | Controls how fonts are embedded into the resulting PDF documents. |
| [EncryptionDetails](encryptiondetails) { get; set; } | Gets or sets the details for encrypting the output PDF document. |
| [ExportDocumentStructure](exportdocumentstructure) { get; set; } | Gets or sets a value determining whether or not to export document structure. |
| [ExportLanguageToSpanTag](exportlanguagetospantag) { get; set; } | Gets or sets a value determining whether or not to create a "Span" tag in the document structure to export the text language. |
| [FontEmbeddingMode](fontembeddingmode) { get; set; } | Specifies the font embedding mode. |
| [HeaderFooterBookmarksExportMode](headerfooterbookmarksexportmode) { get; set; } | Determines how bookmarks in headers/footers are exported. |
| [ImageColorSpaceExportMode](imagecolorspaceexportmode) { get; set; } | Specifies how the color space will be selected for the images in PDF document. |
| [ImageCompression](imagecompression) { get; set; } | Specifies compression type to be used for all images in the document. |
| [InterpolateImages](interpolateimages) { get; set; } | A flag indicating whether image interpolation shall be performed by a conforming reader. When `false` is specified, the flag is not written to the output document and the default behaviour of reader is used instead. |
| [JpegQuality](jpegquality) { get; set; } | Gets or sets a value determining the quality of the JPEG images inside PDF document. |
| [OpenHyperlinksInNewWindow](openhyperlinksinnewwindow) { get; set; } | Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |
| [OutlineOptions](outlineoptions) { get; } | Allows to specify outline options. |
| [PageMode](pagemode) { get; set; } | Specifies how the PDF document should be displayed when opened in the PDF reader. |
| [PreblendImages](preblendimages) { get; set; } | Gets or sets a value determining whether or not to preblend transparent images with black background color. |
| [PreserveFormFields](preserveformfields) { get; set; } | Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is `false`. |
| override [SaveFormat](saveformat) { get; set; } | Specifies the format in which the document will be saved if this save options object is used. Can only be Pdf. |
| [TextCompression](textcompression) { get; set; } | Specifies compression type to be used for all textual content in the document. |
| [UseBookFoldPrintingSettings](usebookfoldprintingsettings) { get; set; } | Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [`MultiplePages`](../../aspose.words/pagesetup/multiplepages). |
| [UseCoreFonts](usecorefonts) { get; set; } | Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |
| [ZoomBehavior](zoombehavior) { get; set; } | Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. |
| [ZoomFactor](zoomfactor) { get; set; } | Gets or sets a value determining zoom factor (in percentages) for a document. |
| [Clone](clone)() | Creates a deep clone of this object. |

### See Also

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* namespace [Aspose.Words.Saving](../../aspose.words.saving)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
