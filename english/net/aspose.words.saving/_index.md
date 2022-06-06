---
title: Aspose.Words.Saving
second_title: Aspose.Words for .NET API Reference
description: The Aspose.Words.Saving namespace provides classes and enumerations that allow to specify additional options for saving or converting documents.
type: docs
weight: 220
url: /net/aspose.words.saving/
---
The **Aspose.Words.Saving** namespace provides classes and enumerations that allow to specify additional options for saving or converting documents.

## Classes

| Class | Description |
| --- | --- |
| class [BookmarksOutlineLevelCollection](./bookmarksoutlinelevelcollection) | A collection of individual bookmarks outline level. |
| class [CssSavingArgs](./csssavingargs) | Provides data for the [`CssSaving`](../aspose.words.saving/icsssavingcallback/csssaving) event. |
| class [DocSaveOptions](./docsaveoptions) | Can be used to specify additional options when saving a document into the Doc or Dot format. |
| class [DocumentPartSavingArgs](./documentpartsavingargs) | Provides data for the [`DocumentPartSaving`](../aspose.words.saving/idocumentpartsavingcallback/documentpartsaving) callback. |
| class [DocumentSavingArgs](./documentsavingargs) | An argument passed into [`Notify`](../aspose.words.saving/idocumentsavingcallback/notify). |
| class [DownsampleOptions](./downsampleoptions) | Allows to specify downsample options. |
| abstract class [FixedPageSaveOptions](./fixedpagesaveoptions) | Contains common options that can be specified when saving a document into fixed page formats (PDF, XPS, images etc). |
| class [FontSavingArgs](./fontsavingargs) | Provides data for the [`FontSaving`](../aspose.words.saving/ifontsavingcallback/fontsaving) event. |
| class [GraphicsQualityOptions](./graphicsqualityoptions) | Allows to specify additional Graphics quality options. |
| class [HtmlFixedSaveOptions](./htmlfixedsaveoptions) | Can be used to specify additional options when saving a document into the HtmlFixed format. |
| class [HtmlSaveOptions](./htmlsaveoptions) | Can be used to specify additional options when saving a document into the Html, Mhtml or Epub format. |
| class [ImageSaveOptions](./imagesaveoptions) | Allows to specify additional options when rendering document pages or shapes to images. |
| class [ImageSavingArgs](./imagesavingargs) | Provides data for the [`ImageSaving`](../aspose.words.saving/iimagesavingcallback/imagesaving) event. |
| class [MarkdownSaveOptions](./markdownsaveoptions) | Class to specify additional options when saving a document into the Markdown format. |
| class [MetafileRenderingOptions](./metafilerenderingoptions) | Allows to specify additional metafile rendering options. |
| class [OdtSaveOptions](./odtsaveoptions) | Can be used to specify additional options when saving a document into the Odt or Ott format. |
| class [OoxmlSaveOptions](./ooxmlsaveoptions) | Can be used to specify additional options when saving a document into the Docx, Docm, Dotx, Dotm or FlatOpc format. |
| class [OutlineOptions](./outlineoptions) | Allows to specify outline options. |
| class [PageRange](./pagerange) | Represents a continuous range of pages. |
| class [PageSavingArgs](./pagesavingargs) | Provides data for the [`PageSaving`](../aspose.words.saving/ipagesavingcallback/pagesaving) event. |
| class [PageSet](./pageset) | Describes a random set of pages. |
| class [PclSaveOptions](./pclsaveoptions) | Can be used to specify additional options when saving a document into the Pcl format. |
| class [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails) | Contains details for signing a PDF document with a digital signature. |
| class [PdfDigitalSignatureTimestampSettings](./pdfdigitalsignaturetimestampsettings) | Contains settings of the digital signature timestamp. |
| class [PdfEncryptionDetails](./pdfencryptiondetails) | Contains details for encrypting and access permissions for a PDF document. |
| class [PdfSaveOptions](./pdfsaveoptions) | Can be used to specify additional options when saving a document into the Pdf format. |
| class [PsSaveOptions](./pssaveoptions) | Can be used to specify additional options when saving a document into the Ps format. |
| class [ResourceSavingArgs](./resourcesavingargs) | Provides data for the [`ResourceSaving`](../aspose.words.saving/iresourcesavingcallback/resourcesaving) event. |
| class [RtfSaveOptions](./rtfsaveoptions) | Can be used to specify additional options when saving a document into the Rtf format. |
| abstract class [SaveOptions](./saveoptions) | This is an abstract base class for classes that allow the user to specify additional options when saving a document into a particular format. |
| class [SaveOutputParameters](./saveoutputparameters) | This object is returned to the caller after a document is saved and contains additional information that has been generated or calculated during the save operation. The caller can use or ignore this object. |
| class [SvgSaveOptions](./svgsaveoptions) | Can be used to specify additional options when saving a document into the Svg format. |
| class [TxtListIndentation](./txtlistindentation) | Specifies how list levels are indented when document is exporting to Text format. |
| class [TxtSaveOptions](./txtsaveoptions) | Can be used to specify additional options when saving a document into the Text format. |
| abstract class [TxtSaveOptionsBase](./txtsaveoptionsbase) | The base class for specifying additional options when saving a document into a text based formats. |
| class [WordML2003SaveOptions](./wordml2003saveoptions) | Can be used to specify additional options when saving a document into the WordML format. |
| class [XamlFixedSaveOptions](./xamlfixedsaveoptions) | Can be used to specify additional options when saving a document into the XamlFixed format. |
| class [XamlFlowSaveOptions](./xamlflowsaveoptions) | Can be used to specify additional options when saving a document into the XamlFlow or XamlFlowPack format. |
| class [XpsSaveOptions](./xpssaveoptions) | Can be used to specify additional options when saving a document into the Xps format. |
## Interfaces

| Interface | Description |
| --- | --- |
| interface [ICssSavingCallback](./icsssavingcallback) | Implement this interface if you want to control how Aspose.Words saves CSS (Cascading Style Sheet) when saving a document to HTML. |
| interface [IDocumentPartSavingCallback](./idocumentpartsavingcallback) | Implement this interface if you want to receive notifications and control how Aspose.Words saves document parts when exporting a document to Html or Epub format. |
| interface [IDocumentSavingCallback](./idocumentsavingcallback) | Implement this interface if you want to have your own custom method called during saving a document. |
| interface [IFontSavingCallback](./ifontsavingcallback) | Implement this interface if you want to receive notifications and control how Aspose.Words saves fonts when exporting a document to HTML format. |
| interface [IImageSavingCallback](./iimagesavingcallback) | Implement this interface if you want to control how Aspose.Words saves images when saving a document to HTML. May be used by other formats. |
| interface [IPageSavingCallback](./ipagesavingcallback) | Implement this interface if you want to control how Aspose.Words saves separate pages when saving a document to fixed page formats. |
| interface [IResourceSavingCallback](./iresourcesavingcallback) | Implement this interface if you want to control how Aspose.Words saves external resources (images, fonts and css) when saving a document to fixed page HTML or SVG. |
## Enumeration

| Enumeration | Description |
| --- | --- |
| enum [ColorMode](./colormode) | Specifies how colors are rendered. |
| enum [CompressionLevel](./compressionlevel) | Compression level for OOXML files. |
| enum [CssStyleSheetType](./cssstylesheettype) | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML. |
| enum [Dml3DEffectsRenderingMode](./dml3deffectsrenderingmode) | Specifies how 3D shape effects are rendered. |
| enum [DmlEffectsRenderingMode](./dmleffectsrenderingmode) | Specifies how DrawingML effects are rendered to fixed page formats. |
| enum [DmlRenderingMode](./dmlrenderingmode) | Specifies how DrawingML shapes are rendered to fixed page formats. |
| enum [DocumentSplitCriteria](./documentsplitcriteria) | Specifies how the document is split into parts when saving to Html or Epub format. |
| enum [EmfPlusDualRenderingMode](./emfplusdualrenderingmode) | Specifies how Aspose.Words should render EMF+ Dual metafiles. |
| enum [ExportFontFormat](./exportfontformat) | Indicates the format that is used to export fonts while rendering to HTML fixed format. |
| enum [ExportHeadersFootersMode](./exportheadersfootersmode) | Specifies how headers and footers are exported to HTML, MHTML or EPUB. |
| enum [ExportListLabels](./exportlistlabels) | Specifies how list labels are exported to HTML, MHTML and EPUB. |
| enum [HeaderFooterBookmarksExportMode](./headerfooterbookmarksexportmode) | Specifies how bookmarks in headers/footers are exported. |
| enum [HtmlElementSizeOutputMode](./htmlelementsizeoutputmode) | Specifies how Aspose.Words exports element widths and heights to HTML, MHTML and EPUB. |
| enum [HtmlFixedPageHorizontalAlignment](./htmlfixedpagehorizontalalignment) | Specifies the horizontal alignment for pages in output HTML document. |
| enum [HtmlMetafileFormat](./htmlmetafileformat) | Indicates the format in which metafiles are saved to HTML documents. |
| enum [HtmlOfficeMathOutputMode](./htmlofficemathoutputmode) | Specifies how Aspose.Words exports OfficeMath to HTML, MHTML and EPUB. |
| enum [HtmlVersion](./htmlversion) | Indicates the version of HTML is used when saving the document to Html and Mhtml formats. |
| enum [ImageBinarizationMethod](./imagebinarizationmethod) | Specifies the method used to binarize image. |
| enum [ImageColorMode](./imagecolormode) | Specifies the color mode for the generated images of document pages. |
| enum [ImagePixelFormat](./imagepixelformat) | Specifies the pixel format for the generated images of document pages. |
| enum [ImlRenderingMode](./imlrenderingmode) | Specifies how ink (InkML) objects are rendered to fixed page formats. |
| enum [MetafileRenderingMode](./metafilerenderingmode) | Specifies how Aspose.Words should render WMF and EMF metafiles. |
| enum [NumeralFormat](./numeralformat) | Indicates the symbol set that is used to represent numbers while rendering to fixed page formats. |
| enum [OdtSaveMeasureUnit](./odtsavemeasureunit) | Specified units of measure to apply to measurable document content such as shape, widths and other during saving. |
| enum [OoxmlCompliance](./ooxmlcompliance) | Allows to specify which OOXML specification will be used when saving in the DOCX format. |
| enum [PdfCompliance](./pdfcompliance) | Specifies the PDF standards compliance level. |
| enum [PdfCustomPropertiesExport](./pdfcustompropertiesexport) | Specifies the way [`CustomDocumentProperties`](../aspose.words/document/customdocumentproperties) are exported to PDF file. |
| enum [PdfDigitalSignatureHashAlgorithm](./pdfdigitalsignaturehashalgorithm) | Specifies a digital hash algorithm used by a digital signature. |
| enum [PdfFontEmbeddingMode](./pdffontembeddingmode) | Specifies how Aspose.Words should embed fonts. |
| enum [PdfImageColorSpaceExportMode](./pdfimagecolorspaceexportmode) | Specifies how the color space will be selected for the images in PDF document. |
| enum [PdfImageCompression](./pdfimagecompression) | Specifies the type of compression applied to images in the PDF file. |
| enum [PdfPageMode](./pdfpagemode) | Specifies how the PDF document should be displayed when opened in the PDF reader. |
| enum [PdfPermissions](./pdfpermissions) | Specifies the operations that are allowed to a user on an encrypted PDF document. |
| enum [PdfTextCompression](./pdftextcompression) | Specifies a type of compression applied to all content in the PDF file except images. |
| enum [PdfZoomBehavior](./pdfzoombehavior) | Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer. |
| enum [SvgTextOutputMode](./svgtextoutputmode) |  |
| enum [TableContentAlignment](./tablecontentalignment) | Allows to specify the alignment of the content of the table to be used when exporting into Markdown format. |
| enum [TiffCompression](./tiffcompression) | Specifies what type of compression to apply when saving page images into a TIFF file. |
| enum [TxtExportHeadersFootersMode](./txtexportheadersfootersmode) | Specifies the way headers and footers are exported to plain text format. |

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
