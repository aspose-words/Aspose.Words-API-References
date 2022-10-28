---
title: 'Aspose::Words::Saving'
second_title: Aspose.Words for C++ API Reference
description: The Aspose.Words.Saving namespace provides classes and enumerations that allow to specify additional options for saving or converting documents.
type: docs
weight: 248
url: /cpp/aspose.words.saving/
---

The **Aspose.Words.Saving** namespace provides classes and enumerations that allow to specify additional options for saving or converting documents.

## Classes

| Class | Description |
| --- | --- |
| [BookmarksOutlineLevelCollection](./bookmarksoutlinelevelcollection/) | A collection of individual bookmarks outline level. |
| [CssSavingArgs](./csssavingargs/) | Provides data for the [CssSaving()](./icsssavingcallback/csssaving/) event. |
| [DocSaveOptions](./docsaveoptions/) | Can be used to specify additional options when saving a document into the **Doc** or **Dot** format. |
| [DocumentPartSavingArgs](./documentpartsavingargs/) | Provides data for the [DocumentPartSaving()](./idocumentpartsavingcallback/documentpartsaving/) callback. |
| [DocumentSavingArgs](./documentsavingargs/) | An argument passed into [Notify()](./idocumentsavingcallback/notify/). |
| [DownsampleOptions](./downsampleoptions/) | Allows to specify downsample options. |
| [FixedPageSaveOptions](./fixedpagesaveoptions/) | Contains common options that can be specified when saving a document into fixed page formats (PDF, XPS, images etc). |
| [FontSavingArgs](./fontsavingargs/) | Provides data for the [FontSaving()](./ifontsavingcallback/fontsaving/) event. |
| [HtmlFixedSaveOptions](./htmlfixedsaveoptions/) | Can be used to specify additional options when saving a document into the **HtmlFixed** format. |
| [HtmlSaveOptions](./htmlsaveoptions/) | Can be used to specify additional options when saving a document into the **Html**, **Mhtml**, **Epub** or **Azw3** format. |
| [ImageSaveOptions](./imagesaveoptions/) | Allows to specify additional options when rendering document pages or shapes to images. |
| [ImageSavingArgs](./imagesavingargs/) | Provides data for the [ImageSaving()](./iimagesavingcallback/imagesaving/) event. |
| [MarkdownSaveOptions](./markdownsaveoptions/) | Class to specify additional options when saving a document into the **Markdown** format. |
| [MetafileRenderingOptions](./metafilerenderingoptions/) | Allows to specify additional metafile rendering options. |
| [OdtSaveOptions](./odtsaveoptions/) | Can be used to specify additional options when saving a document into the **Odt** or **Ott** format. |
| [OoxmlSaveOptions](./ooxmlsaveoptions/) | Can be used to specify additional options when saving a document into the **Docx**, **Docm**, **Dotx**, **Dotm** or **FlatOpc** format. |
| [OutlineOptions](./outlineoptions/) | Allows to specify outline options. |
| [PageRange](./pagerange/) | Represents a continuous range of pages. |
| [PageSavingArgs](./pagesavingargs/) | Provides data for the [PageSaving()](./ipagesavingcallback/pagesaving/) event. |
| [PageSet](./pageset/) | Describes a random set of pages. |
| [PclSaveOptions](./pclsaveoptions/) | Can be used to specify additional options when saving a document into the **Pcl** format. |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/) | Contains details for signing a PDF document with a digital signature. |
| [PdfDigitalSignatureTimestampSettings](./pdfdigitalsignaturetimestampsettings/) | Contains settings of the digital signature timestamp. |
| [PdfEncryptionDetails](./pdfencryptiondetails/) | Contains details for encrypting and access permissions for a PDF document. |
| [PdfSaveOptions](./pdfsaveoptions/) | Can be used to specify additional options when saving a document into the **Pdf** format. |
| [PsSaveOptions](./pssaveoptions/) | Can be used to specify additional options when saving a document into the **Ps** format. |
| [ResourceSavingArgs](./resourcesavingargs/) | Provides data for the [ResourceSaving()](./iresourcesavingcallback/resourcesaving/) event. |
| [RtfSaveOptions](./rtfsaveoptions/) | Can be used to specify additional options when saving a document into the **Rtf** format. |
| [SaveOptions](./saveoptions/) | This is an abstract base class for classes that allow the user to specify additional options when saving a document into a particular format. To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/net/specify-save-options/) documentation article. |
| [SaveOutputParameters](./saveoutputparameters/) | This object is returned to the caller after a document is saved and contains additional information that has been generated or calculated during the save operation. The caller can use or ignore this object. |
| [SvgSaveOptions](./svgsaveoptions/) | Can be used to specify additional options when saving a document into the **Svg** format. |
| [TxtListIndentation](./txtlistindentation/) | Specifies how list levels are indented when document is exporting to **Text** format. |
| [TxtSaveOptions](./txtsaveoptions/) | Can be used to specify additional options when saving a document into the **Text** format. |
| [TxtSaveOptionsBase](./txtsaveoptionsbase/) | The base class for specifying additional options when saving a document into a text based formats. |
| [WordML2003SaveOptions](./wordml2003saveoptions/) | Can be used to specify additional options when saving a document into the **WordML** format. |
| [XamlFixedSaveOptions](./xamlfixedsaveoptions/) | Can be used to specify additional options when saving a document into the **XamlFixed** format. |
| [XamlFlowSaveOptions](./xamlflowsaveoptions/) | Can be used to specify additional options when saving a document into the **XamlFlow** or **XamlFlowPack** format. |
| [XpsSaveOptions](./xpssaveoptions/) | Can be used to specify additional options when saving a document into the **Xps** format. |
## Interfaces

| Interface | Description |
| --- | --- |
| [ICssSavingCallback](./icsssavingcallback/) | Implement this interface if you want to control how Aspose.Words saves CSS (Cascading [Style](../aspose.words/style/) Sheet) when saving a document to HTML. |
| [IDocumentPartSavingCallback](./idocumentpartsavingcallback/) | Implement this interface if you want to receive notifications and control how Aspose.Words saves document parts when exporting a document to **Html** or **Epub** format. |
| [IDocumentSavingCallback](./idocumentsavingcallback/) | Implement this interface if you want to have your own custom method called during saving a document. |
| [IFontSavingCallback](./ifontsavingcallback/) | Implement this interface if you want to receive notifications and control how Aspose.Words saves fonts when exporting a document to HTML format. |
| [IImageSavingCallback](./iimagesavingcallback/) | Implement this interface if you want to control how Aspose.Words saves images when saving a document to HTML. May be used by other formats. |
| [IPageSavingCallback](./ipagesavingcallback/) | Implement this interface if you want to control how Aspose.Words saves separate pages when saving a document to fixed page formats. |
| [IResourceSavingCallback](./iresourcesavingcallback/) | Implement this interface if you want to control how Aspose.Words saves external resources (images, fonts and css) when saving a document to fixed page HTML or SVG. |
## Enums

| Enum | Description |
| --- | --- |
| [ColorMode](./colormode/) | Specifies how colors are rendered. |
| [CompressionLevel](./compressionlevel/) | Compression level for OOXML files. (DOCX and DOTX files are internally a ZIP-archive, this property controls the compression level of the archive. Note, that FlatOpc file is not a ZIP-archive, therefore, this property does not affect the FlatOpc files.) |
| [CssStyleSheetType](./cssstylesheettype/) | Specifies how CSS (Cascading [Style](../aspose.words/style/) Sheet) styles are exported to HTML. |
| [Dml3DEffectsRenderingMode](./dml3deffectsrenderingmode/) | Specifies how 3D shape effects are rendered. |
| [DmlEffectsRenderingMode](./dmleffectsrenderingmode/) | Specifies how DrawingML effects are rendered to fixed page formats. |
| [DmlRenderingMode](./dmlrenderingmode/) | Specifies how DrawingML shapes are rendered to fixed page formats. |
| [DocumentSplitCriteria](./documentsplitcriteria/) | Specifies how the document is split into parts when saving to **Html**, **Epub** or **Azw3** format. |
| [EmfPlusDualRenderingMode](./emfplusdualrenderingmode/) | Specifies how Aspose.Words should render EMF+ Dual metafiles. |
| [ExportFontFormat](./exportfontformat/) | Indicates the format that is used to export fonts while rendering to HTML fixed format. |
| [ExportHeadersFootersMode](./exportheadersfootersmode/) | Specifies how headers and footers are exported to HTML, MHTML or EPUB. |
| [ExportListLabels](./exportlistlabels/) | Specifies how list labels are exported to HTML, MHTML and EPUB. |
| [HeaderFooterBookmarksExportMode](./headerfooterbookmarksexportmode/) | Specifies how bookmarks in headers/footers are exported. |
| [HtmlElementSizeOutputMode](./htmlelementsizeoutputmode/) | Specifies how Aspose.Words exports element widths and heights to HTML, MHTML and EPUB. |
| [HtmlFixedPageHorizontalAlignment](./htmlfixedpagehorizontalalignment/) | Specifies the horizontal alignment for pages in output HTML document. |
| [HtmlMetafileFormat](./htmlmetafileformat/) | Indicates the format in which metafiles are saved to HTML documents. |
| [HtmlOfficeMathOutputMode](./htmlofficemathoutputmode/) | Specifies how Aspose.Words exports OfficeMath to HTML, MHTML and EPUB. |
| [HtmlVersion](./htmlversion/) | Indicates the version of HTML is used when saving the document to **Html** and **Mhtml** formats. |
| [ImageBinarizationMethod](./imagebinarizationmethod/) | Specifies the method used to binarize image. |
| [ImageColorMode](./imagecolormode/) | Specifies the color mode for the generated images of document pages. |
| [ImagePixelFormat](./imagepixelformat/) | Specifies the pixel format for the generated images of document pages. |
| [ImlRenderingMode](./imlrenderingmode/) | Specifies how ink (InkML) objects are rendered to fixed page formats. |
| [MetafileRenderingMode](./metafilerenderingmode/) | Specifies how Aspose.Words should render WMF and EMF metafiles. |
| [NumeralFormat](./numeralformat/) | Indicates the symbol set that is used to represent numbers while rendering to fixed page formats. |
| [OdtSaveMeasureUnit](./odtsavemeasureunit/) | Specified units of measure to apply to measurable document content such as shape, widths and other during saving. |
| [OoxmlCompliance](./ooxmlcompliance/) | Allows to specify which OOXML specification will be used when saving in the DOCX format. |
| [PdfCompliance](./pdfcompliance/) | Specifies the PDF standards compliance level. |
| [PdfCustomPropertiesExport](./pdfcustompropertiesexport/) | Specifies the way [CustomDocumentProperties](../aspose.words/document/get_customdocumentproperties/) are exported to PDF file. |
| [PdfDigitalSignatureHashAlgorithm](./pdfdigitalsignaturehashalgorithm/) | Specifies a digital hash algorithm used by a digital signature. |
| [PdfFontEmbeddingMode](./pdffontembeddingmode/) | Specifies how Aspose.Words should embed fonts. |
| [PdfImageColorSpaceExportMode](./pdfimagecolorspaceexportmode/) | Specifies how the color space will be selected for the images in PDF document. |
| [PdfImageCompression](./pdfimagecompression/) | Specifies the type of compression applied to images in the PDF file. |
| [PdfPageMode](./pdfpagemode/) | Specifies how the PDF document should be displayed when opened in the PDF reader. |
| [PdfPermissions](./pdfpermissions/) | Specifies the operations that are allowed to a user on an encrypted PDF document. |
| [PdfTextCompression](./pdftextcompression/) | Specifies a type of compression applied to all content in the PDF file except images. |
| [PdfZoomBehavior](./pdfzoombehavior/) | Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer. |
| [SvgTextOutputMode](./svgtextoutputmode/) |  |
| [TableContentAlignment](./tablecontentalignment/) | Allows to specify the alignment of the content of the table to be used when exporting into Markdown format. |
| [TiffCompression](./tiffcompression/) | Specifies what type of compression to apply when saving page images into a TIFF file. |
| [TxtExportHeadersFootersMode](./txtexportheadersfootersmode/) | Specifies the way headers and footers are exported to plain text format. |
