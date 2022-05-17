---
title: HtmlSaveOptions
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 4800
url: /net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Can be used to specify additional options when saving a document into the Html, Mhtml or Epub format.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions)() | Initializes a new instance of this class that can be used to save a document in the Html format. |
| [HtmlSaveOptions](htmlsaveoptions)(SaveFormat) | Initializes a new instance of this class that can be used to save a document in the Html, Mhtml or Epub format. |

## Properties

| Name | Description |
| --- | --- |
| [AllowNegativeIndent](allownegativeindent) { get; set; } | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is `false`. |
| [CssClassNamePrefix](cssclassnameprefix) { get; set; } | Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix. |
| [CssSavingCallback](csssavingcallback) { get; set; } | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [CssStyleSheetFileName](cssstylesheetfilename) { get; set; } | Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string. |
| [CssStyleSheetType](cssstylesheettype) { get; set; } | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is Inline for HTML/MHTML and External for EPUB. |
| [DocumentPartSavingCallback](documentpartsavingcallback) { get; set; } | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [DocumentSplitCriteria](documentsplitcriteria) { get; set; } | Specifies how the document should be split when saving to Html or Epub format. Default is None for HTML and HeadingParagraph for EPUB. |
| [DocumentSplitHeadingLevel](documentsplitheadinglevel) { get; set; } | Specifies the maximum level of headings at which to split the document. Default value is `2`. |
| [Encoding](encoding) { get; set; } | Specifies the encoding to use when exporting to HTML, MHTML or EPUB. Default value is `new UTF8Encoding(false)` (UTF-8 without BOM). |
| [EpubNavigationMapLevel](epubnavigationmaplevel) { get; set; } | Specifies the maximum level of headings populated to the navigation map when exporting to IDPF EPUB format. Default value is `3`. |
| [ExportCidUrlsForMhtmlResources](exportcidurlsformhtmlresources) { get; set; } | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is `false`. |
| [ExportDocumentProperties](exportdocumentproperties) { get; set; } | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is `false`. |
| [ExportDropDownFormFieldAsText](exportdropdownformfieldastext) { get; set; } | Controls how drop-down form fields are saved to HTML or MHTML. Default value is `false`. |
| [ExportFontResources](exportfontresources) { get; set; } | Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is `false`. |
| [ExportFontsAsBase64](exportfontsasbase64) { get; set; } | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is `false`. |
| [ExportHeadersFootersMode](exportheadersfootersmode) { get; set; } | Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is PerSection for HTML/MHTML and None for EPUB. |
| [ExportImagesAsBase64](exportimagesasbase64) { get; set; } | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is `false`. |
| [ExportLanguageInformation](exportlanguageinformation) { get; set; } | Specifies whether language information is exported to HTML, MHTML or EPUB. Default is `false`. |
| [ExportListLabels](exportlistlabels) { get; set; } | Controls how list labels are output to HTML, MHTML or EPUB. Default value is Auto. |
| [ExportOriginalUrlForLinkedImages](exportoriginalurlforlinkedimages) { get; set; } | Specifies whether original URL should be used as the URL of the linked images. Default value is `false`. |
| [ExportPageMargins](exportpagemargins) { get; set; } | Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is `false`. |
| [ExportPageSetup](exportpagesetup) { get; set; } | Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is `false`. |
| [ExportRelativeFontSize](exportrelativefontsize) { get; set; } | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is `false`. |
| [ExportRoundtripInformation](exportroundtripinformation) { get; set; } | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is `true` for HTML and `false` for MHTML and EPUB. |
| [ExportShapesAsSvg](exportshapesassvg) { get; set; } | Controls whether [`Shape`](../../aspose.words.drawing/shape) nodes are converted to SVG images when saving to HTML, MHTML or EPUB. Default value is `false`. |
| [ExportTextInputFormFieldAsText](exporttextinputformfieldastext) { get; set; } | Controls how text input form fields are saved to HTML or MHTML. Default value is `false`. |
| [ExportTocPageNumbers](exporttocpagenumbers) { get; set; } | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is `false`. |
| [ExportXhtmlTransitional](exportxhtmltransitional) { get; set; } | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When `true`, writes a DOCTYPE declaration in the document prior to the root element. Default value is `false`. When saving to EPUB or HTML5 (Html5) the DOCTYPE declaration is always written. |
| [FontResourcesSubsettingSizeThreshold](fontresourcessubsettingsizethreshold) { get; set; } | Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is `0`. |
| [FontSavingCallback](fontsavingcallback) { get; set; } | Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB. |
| [FontsFolder](fontsfolder) { get; set; } | Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string. |
| [FontsFolderAlias](fontsfolderalias) { get; set; } | Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string. |
| [HtmlVersion](htmlversion) { get; set; } | Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is Xhtml. |
| [ImageResolution](imageresolution) { get; set; } | Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is `96 dpi`. |
| [ImageSavingCallback](imagesavingcallback) { get; set; } | Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB. |
| [ImagesFolder](imagesfolder) { get; set; } | Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string. |
| [ImagesFolderAlias](imagesfolderalias) { get; set; } | Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string. |
| [MetafileFormat](metafileformat) { get; set; } | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is Png, meaning that metafiles are rendered to raster PNG images. |
| [OfficeMathOutputMode](officemathoutputmode) { get; set; } | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is `HtmlOfficeMathOutputMode.Image`. |
| [ResolveFontNames](resolvefontnames) { get; set; } | Specifies whether font family names used in the document are resolved and substituted according to [`FontSettings`](../../aspose.words/document/fontsettings) when being written into HTML-based formats. |
| [ResourceFolder](resourcefolder) { get; set; } | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string. |
| [ResourceFolderAlias](resourcefolderalias) { get; set; } | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string. |
| override [SaveFormat](saveformat) { get; set; } | Specifies the format in which the document will be saved if this save options object is used. Can be Html, Mhtml or Epub. |
| [ScaleImageToShapeSize](scaleimagetoshapesize) { get; set; } | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is `true`. |
| [TableWidthOutputMode](tablewidthoutputmode) { get; set; } | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is All. |

### See Also

* class [SaveOptions](../saveoptions)
* namespace [Aspose.Words.Saving](../../aspose.words.saving)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
