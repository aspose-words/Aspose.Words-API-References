---
title: HtmlSaveOptions class
linktitle: HtmlSaveOptions class
articleTitle: HtmlSaveOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.HtmlSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.Html](../../aspose.words/saveformat/#Html), [SaveFormat.Mhtml](../../aspose.words/saveformat/#Mhtml), [SaveFormat.Epub](../../aspose.words/saveformat/#Epub), [SaveFormat.Azw3](../../aspose.words/saveformat/#Azw3) or [SaveFormat.Mobi](../../aspose.words/saveformat/#Mobi) format"
type: docs
weight: 280
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/
---

## HtmlSaveOptions class

Can be used to specify additional options when saving a document into the
[SaveFormat.Html](../../aspose.words/saveformat/#Html), [SaveFormat.Mhtml](../../aspose.words/saveformat/#Mhtml), [SaveFormat.Epub](../../aspose.words/saveformat/#Epub),
[SaveFormat.Azw3](../../aspose.words/saveformat/#Azw3) or [SaveFormat.Mobi](../../aspose.words/saveformat/#Mobi) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [HtmlSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [HtmlSaveOptions()](./constructor/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Html](../../aspose.words/saveformat/#Html) format. |
| [HtmlSaveOptions(saveFormat)](./constructor/#saveformat) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Html](../../aspose.words/saveformat/#Html), [SaveFormat.Mhtml](../../aspose.words/saveformat/#Mhtml), [SaveFormat.Epub](../../aspose.words/saveformat/#Epub), [SaveFormat.Azw3](../../aspose.words/saveformat/#Azw3) or [SaveFormat.Mobi](../../aspose.words/saveformat/#Mobi) format. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [allowNegativeIndent](./allowNegativeIndent/) | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is ``false``. |
| [cssClassNamePrefix](./cssClassNamePrefix/) | Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix. |
| [cssSavingCallback](./cssSavingCallback/) | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [cssStyleSheetFileName](./cssStyleSheetFileName/) | Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string. |
| [cssStyleSheetType](./cssStyleSheetType/) | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [CssStyleSheetType.Inline](../cssstylesheettype/#Inline) for HTML/MHTML and [CssStyleSheetType.External](../cssstylesheettype/#External) for EPUB. |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** .<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [documentPartSavingCallback](./documentPartSavingCallback/) | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [documentSplitCriteria](./documentSplitCriteria/) | Specifies how the document should be split when saving to [SaveFormat.Html](../../aspose.words/saveformat/#Html), [SaveFormat.Epub](../../aspose.words/saveformat/#Epub) or [SaveFormat.Azw3](../../aspose.words/saveformat/#Azw3) format. Default is [DocumentSplitCriteria.None](../documentsplitcriteria/#None) for HTML and [DocumentSplitCriteria.HeadingParagraph](../documentsplitcriteria/#HeadingParagraph) for EPUB and AZW3. |
| [documentSplitHeadingLevel](./documentSplitHeadingLevel/) | Specifies the maximum level of headings at which to split the document. Default value is ``2``. |
| [encoding](./encoding/) | Specifies the encoding to use when exporting to HTML, MHTML or EPUB. Default value is . |
| [exportCidUrlsForMhtmlResources](./exportCidUrlsForMhtmlResources/) | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is ``false``. |
| [exportDocumentProperties](./exportDocumentProperties/) | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is ``false``. |
| [exportDropDownFormFieldAsText](./exportDropDownFormFieldAsText/) | Controls how drop-down form fields are saved to HTML or MHTML. Default value is ``false``. |
| [exportFontResources](./exportFontResources/) | Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is ``false``. |
| [exportFontsAsBase64](./exportFontsAsBase64/) | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is ``false``. |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``true``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportHeadersFootersMode](./exportHeadersFootersMode/) | Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is [ExportHeadersFootersMode.PerSection](../exportheadersfootersmode/#PerSection) for HTML/MHTML and [ExportHeadersFootersMode.None](../exportheadersfootersmode/#None) for EPUB. |
| [exportImagesAsBase64](./exportImagesAsBase64/) | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is ``false``. |
| [exportLanguageInformation](./exportLanguageInformation/) | Specifies whether language information is exported to HTML, MHTML or EPUB. Default is ``false``. |
| [exportListLabels](./exportListLabels/) | Controls how list labels are output to HTML, MHTML or EPUB. Default value is [ExportListLabels.Auto](../exportlistlabels/#Auto). |
| [exportOriginalUrlForLinkedImages](./exportOriginalUrlForLinkedImages/) | Specifies whether original URL should be used as the URL of the linked images. Default value is ``false``. |
| [exportPageMargins](./exportPageMargins/) | Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is ``false``. |
| [exportPageSetup](./exportPageSetup/) | Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is ``false``. |
| [exportRelativeFontSize](./exportRelativeFontSize/) | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is ``false``. |
| [exportRoundtripInformation](./exportRoundtripInformation/) | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is ``true`` for HTML and ``false`` for MHTML and EPUB. |
| [exportShapesAsSvg](./exportShapesAsSvg/) | Controls whether [Shape](../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is ``false``. |
| [exportTextInputFormFieldAsText](./exportTextInputFormFieldAsText/) | Controls how text input form fields are saved to HTML or MHTML. Default value is ``false``. |
| [exportTocPageNumbers](./exportTocPageNumbers/) | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is ``false``. |
| [exportXhtmlTransitional](./exportXhtmlTransitional/) | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When ``true``, writes a DOCTYPE declaration in the document prior to the root element. Default value is ``false``. When saving to EPUB or HTML5 ([HtmlVersion.Html5](../htmlversion/#Html5)) the DOCTYPE declaration is always written. |
| [fontResourcesSubsettingSizeThreshold](./fontResourcesSubsettingSizeThreshold/) | Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is ``0``. |
| [fontSavingCallback](./fontSavingCallback/) | Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB. |
| [fontsFolder](./fontsFolder/) | Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string. |
| [fontsFolderAlias](./fontsFolderAlias/) | Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string. |
| [htmlVersion](./htmlVersion/) | Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is [HtmlVersion.Xhtml](../htmlversion/#Xhtml). |
| [imageResolution](./imageResolution/) | Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is ``96 dpi``. |
| [imageSavingCallback](./imageSavingCallback/) | Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB. |
| [imagesFolder](./imagesFolder/) | Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string. |
| [imagesFolderAlias](./imagesFolderAlias/) | Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string. |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafileFormat](./metafileFormat/) | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is [HtmlMetafileFormat.Png](../htmlmetafileformat/#Png), meaning that metafiles are rendered to raster PNG images. |
| [navigationMapLevel](./navigationMapLevel/) | Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats. Default value is ``3``. |
| [officeMathOutputMode](./officeMathOutputMode/) | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is [HtmlOfficeMathOutputMode.Image](../htmlofficemathoutputmode/#Image). |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``true``, pretty formats output where applicable. Default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [removeJavaScriptFromLinks](./removeJavaScriptFromLinks/) | Specifies whether JavaScript will be removed from links. Default is ``false``. |
| [replaceBackslashWithYenSign](./replaceBackslashWithYenSign/) | Specifies whether backslash characters should be replaced with yen signs. Default value is ``false``. |
| [resolveFontNames](./resolveFontNames/) | Specifies whether font family names used in the document are resolved and substituted according to [Document.fontSettings](../../aspose.words/document/fontSettings/) when being written into HTML-based formats. |
| [resourceFolder](./resourceFolder/) | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string. |
| [resourceFolderAlias](./resourceFolderAlias/) | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string. |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.Html](../../aspose.words/saveformat/#Html), [SaveFormat.Mhtml](../../aspose.words/saveformat/#Mhtml), [SaveFormat.Epub](../../aspose.words/saveformat/#Epub), [SaveFormat.Azw3](../../aspose.words/saveformat/#Azw3) or [SaveFormat.Mobi](../../aspose.words/saveformat/#Mobi). |
| [scaleImageToShapeSize](./scaleImageToShapeSize/) | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is ``true``. |
| [tableWidthOutputMode](./tableWidthOutputMode/) | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is [HtmlElementSizeOutputMode.All](../htmlelementsizeoutputmode/#All). |
| [tempFolder](../saveoptions/tempFolder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default, this property is ``null`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateAmbiguousTextFont](../saveoptions/updateAmbiguousTextFont/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateCreatedTimeProperty](../saveoptions/updateCreatedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../aspose.words.properties/builtindocumentproperties/createdTime/) property is updated before saving. Default value is ``false``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateFields](../saveoptions/updateFields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastPrintedProperty](../saveoptions/updateLastPrintedProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../aspose.words.properties/builtindocumentproperties/lastPrinted/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastSavedTimeProperty](../saveoptions/updateLastSavedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../aspose.words.properties/builtindocumentproperties/lastSavedTime/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateOleControlImages](../saveoptions/updateOleControlImages/) | Gets or sets a value determining whether OLE controls presentation image will be updated.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useAntiAliasing](../saveoptions/useAntiAliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useHighQualityRendering](../saveoptions/useHighQualityRendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Methods

| Name | Description |
| --- | --- |
|[ createSaveOptions(saveFormat)](../saveoptions/createSaveOptions/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ createSaveOptions(fileName)](../saveoptions/createSaveOptions/#string) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Examples

Shows how to use a specific encoding when saving a document to .epub.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// Use a SaveOptions object to specify the encoding for a document that we will save.
let saveOptions = new aw.Saving.HtmlSaveOptions();
saveOptions.saveFormat = aw.SaveFormat.Epub;
saveOptions.encoding = "utf-8";

// By default, an output .epub document will have all its contents in one HTML part.
// A split criterion allows us to segment the document into several HTML parts.
// We will set the criteria to split the document into heading paragraphs.
// This is useful for readers who cannot read HTML files more significant than a specific size.
saveOptions.documentSplitCriteria = aw.Saving.DocumentSplitCriteria.HeadingParagraph;

// Specify that we want to export document properties.
saveOptions.exportDocumentProperties = true;

doc.save(base.artifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Shows how to specify the folder for storing linked images after saving to .html.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let imagesDir = path.join(base.artifactsDir, "SaveHtmlWithOptions");

if (fs.existsSync(imagesDir)) {
  fs.rmSync(imagesDir, { recursive: true, force: true });
}

fs.mkdirSync(imagesDir, { recursive: true });

// Set an option to export form fields as plain text instead of HTML input elements.
let options = new aw.Saving.HtmlSaveOptions(aw.SaveFormat.Html);
options.exportTextInputFormFieldAsText = true;
options.imagesFolder = imagesDir;

doc.save(base.artifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### See Also

* module [Aspose.Words.Saving](../)
* class [SaveOptions](../saveoptions/)

