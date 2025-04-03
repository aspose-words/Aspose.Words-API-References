---
title: HtmlSaveOptions class
linktitle: HtmlSaveOptions class
articleTitle: HtmlSaveOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.HtmlSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.Html](../../aspose.words/saveformat/#Html), [SaveFormat.Mhtml](../../aspose.words/saveformat/#Mhtml), [SaveFormat.Epub](../../aspose.words/saveformat/#Epub), [SaveFormat.Azw3](../../aspose.words/saveformat/#Azw3) or [SaveFormat.Mobi](../../aspose.words/saveformat/#Mobi) format"
type: docs
weight: 270
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/
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
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [allowNegativeIndent](./allowNegativeIndent/) | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is ``False``. |
| [cssClassNamePrefix](./cssClassNamePrefix/) | Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix. |
| [cssSavingCallback](./cssSavingCallback/) | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [cssStyleSheetFileName](./cssStyleSheetFileName/) | Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string. |
| [cssStyleSheetType](./cssStyleSheetType/) | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [CssStyleSheetType.Inline](../cssstylesheettype/#Inline) for HTML/MHTML and  [CssStyleSheetType.External](../cssstylesheettype/#External) for EPUB. |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [documentPartSavingCallback](./documentPartSavingCallback/) | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [documentSplitCriteria](./documentSplitCriteria/) | Specifies how the document should be split when saving to [SaveFormat.Html](../../aspose.words/saveformat/#Html), [SaveFormat.Epub](../../aspose.words/saveformat/#Epub) or [SaveFormat.Azw3](../../aspose.words/saveformat/#Azw3) format.  Default is [DocumentSplitCriteria.None](../documentsplitcriteria/#None) for HTML and  [DocumentSplitCriteria.HeadingParagraph](../documentsplitcriteria/#HeadingParagraph) for EPUB and AZW3. |
| [documentSplitHeadingLevel](./documentSplitHeadingLevel/) | Specifies the maximum level of headings at which to split the document. Default value is ``2``. |
| [encoding](./encoding/) | Specifies the encoding to use when exporting to HTML, MHTML or EPUB. Default value is ``new UTF8Encoding(false)`` (UTF-8 without BOM). |
| [exportCidUrlsForMhtmlResources](./exportCidUrlsForMhtmlResources/) | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is ``False``. |
| [exportDocumentProperties](./exportDocumentProperties/) | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is ``False``. |
| [exportDropDownFormFieldAsText](./exportDropDownFormFieldAsText/) | Controls how drop-down form fields are saved to HTML or MHTML. Default value is ``False``. |
| [exportFontResources](./exportFontResources/) | Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is ``False``. |
| [exportFontsAsBase64](./exportFontsAsBase64/) | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is ``False``. |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportHeadersFootersMode](./exportHeadersFootersMode/) | Specifies how headers and footers are output to HTML, MHTML or EPUB.  Default value is [ExportHeadersFootersMode.PerSection](../exportheadersfootersmode/#PerSection) for HTML/MHTML  and [ExportHeadersFootersMode.None](../exportheadersfootersmode/#None) for EPUB. |
| [exportImagesAsBase64](./exportImagesAsBase64/) | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is ``False``. |
| [exportLanguageInformation](./exportLanguageInformation/) | Specifies whether language information is exported to HTML, MHTML or EPUB. Default is ``False``. |
| [exportListLabels](./exportListLabels/) | Controls how list labels are output to HTML, MHTML or EPUB.  Default value is [ExportListLabels.Auto](../exportlistlabels/#Auto). |
| [exportOriginalUrlForLinkedImages](./exportOriginalUrlForLinkedImages/) | Specifies whether original URL should be used as the URL of the linked images. Default value is ``False``. |
| [exportPageMargins](./exportPageMargins/) | Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is ``False``. |
| [exportPageSetup](./exportPageSetup/) | Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is ``False``. |
| [exportRelativeFontSize](./exportRelativeFontSize/) | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is ``False``. |
| [exportRoundtripInformation](./exportRoundtripInformation/) | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is ``True`` for HTML and ``False`` for MHTML and EPUB. |
| [exportShapesAsSvg](./exportShapesAsSvg/) | Controls whether [Shape](../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is ``False``. |
| [exportTextInputFormFieldAsText](./exportTextInputFormFieldAsText/) | Controls how text input form fields are saved to HTML or MHTML. Default value is ``False``. |
| [exportTocPageNumbers](./exportTocPageNumbers/) | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is ``False``. |
| [exportXhtmlTransitional](./exportXhtmlTransitional/) | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When ``True``, writes a DOCTYPE declaration in the document prior to the root element.  Default value is ``False``. When saving to EPUB or HTML5 ([HtmlVersion.Html5](../htmlversion/#Html5)) the DOCTYPE declaration is always written. |
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
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafileFormat](./metafileFormat/) | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is [HtmlMetafileFormat.Png](../htmlmetafileformat/#Png), meaning that metafiles are rendered to raster PNG images. |
| [navigationMapLevel](./navigationMapLevel/) | Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats. Default value is ``3``. |
| [officeMathOutputMode](./officeMathOutputMode/) | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is [HtmlOfficeMathOutputMode.Image](../htmlofficemathoutputmode/#Image). |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [replaceBackslashWithYenSign](./replaceBackslashWithYenSign/) | Specifies whether backslash characters should be replaced with yen signs. Default value is ``False``. |
| [resolveFontNames](./resolveFontNames/) | Specifies whether font family names used in the document are resolved and substituted according to [Document.fontSettings](../../aspose.words/document/fontSettings/) when being written into HTML-based formats. |
| [resourceFolder](./resourceFolder/) | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string. |
| [resourceFolderAlias](./resourceFolderAlias/) | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string. |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.Html](../../aspose.words/saveformat/#Html), [SaveFormat.Mhtml](../../aspose.words/saveformat/#Mhtml), [SaveFormat.Epub](../../aspose.words/saveformat/#Epub), [SaveFormat.Azw3](../../aspose.words/saveformat/#Azw3) or [SaveFormat.Mobi](../../aspose.words/saveformat/#Mobi). |
| [scaleImageToShapeSize](./scaleImageToShapeSize/) | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is ``True``. |
| [tableWidthOutputMode](./tableWidthOutputMode/) | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is [HtmlElementSizeOutputMode.All](../htmlelementsizeoutputmode/#All). |
| [tempFolder](../saveoptions/tempFolder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateAmbiguousTextFont](../saveoptions/updateAmbiguousTextFont/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateCreatedTimeProperty](../saveoptions/updateCreatedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../aspose.words.properties/builtindocumentproperties/createdTime/) property is updated before saving. Default value is ``False``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateFields](../saveoptions/updateFields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastPrintedProperty](../saveoptions/updateLastPrintedProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../aspose.words.properties/builtindocumentproperties/lastPrinted/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastSavedTimeProperty](../saveoptions/updateLastSavedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../aspose.words.properties/builtindocumentproperties/lastSavedTime/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
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

Shows how to split a document into parts and save them.

```js
test('DocumentPartsFileNames', () => {
  let doc = new aw.Document(base.myDir + "Rendering.docx");
  string outFileName = "SavingCallback.DocumentPartsFileNames.html";

  // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
  // to modify how we convert the document to HTML.
  let options = new aw.Saving.HtmlSaveOptions();

  // If we save the document normally, there will be one output HTML
  // document with all the source document's contents.
  // Set the "DocumentSplitCriteria" property to "DocumentSplitCriteria.SectionBreak" to
  // save our document to multiple HTML files: one for each section.
  options.documentSplitCriteria = aw.Saving.DocumentSplitCriteria.SectionBreak;

  // Assign a custom callback to the "DocumentPartSavingCallback" property to alter the document part saving logic.
  options.documentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.documentSplitCriteria);

  // If we convert a document that contains images into html, we will end up with one html file which links to several images.
  // Each image will be in the form of a file in the local file system.
  // There is also a callback that can customize the name and file system location of each image.
  options.imageSavingCallback = new SavedImageRename(outFileName);

  doc.save(base.artifactsDir + outFileName, options);
});


  /// <summary>
  /// Sets custom filenames for output documents that the saving operation splits a document into.
  /// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
  public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
  {
    mOutFileName = outFileName;
    mDocumentSplitCriteria = documentSplitCriteria;
  }

  void aw.Saving.IDocumentPartSavingCallback.documentPartSaving(DocumentPartSavingArgs args)
  {
      // We can access the entire source document via the "Document" property.
    expect(args.document.originalFileName.EndsWith("Rendering.docx")).toEqual(true);

    string partType = '';

    switch (mDocumentSplitCriteria)
    {
      case aw.Saving.DocumentSplitCriteria.PageBreak:
        partType = "Page";
        break;
      case aw.Saving.DocumentSplitCriteria.ColumnBreak:
        partType = "Column";
        break;
      case aw.Saving.DocumentSplitCriteria.SectionBreak:
        partType = "Section";
        break;
      case aw.Saving.DocumentSplitCriteria.HeadingParagraph:
        partType = "Paragraph from heading";
        break;
    }

    string partFileName = `${mOutFileName} part ${++mCount}, of type ${partType}${Path.GetExtension(args.documentPartFileName)}`;

      // Below are two ways of specifying where Aspose.Words will save each part of the document.
      // 1 -  Set a filename for the output part file:
    args.documentPartFileName = partFileName;

      // 2 -  Create a custom stream for the output part file:
    args.documentPartStream = new FileStream(base.artifactsDir + partFileName, FileMode.create);

    expect(args.documentPartStream.CanWrite).toEqual(true);
    expect(args.keepDocumentPartStreamOpen).toEqual(false);
  }

  private int mCount;
  private readonly string mOutFileName;
  private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

  /// <summary>
  /// Sets custom filenames for image files that an HTML conversion creates.
  /// </summary>
public class SavedImageRename : IImageSavingCallback
{
  public SavedImageRename(string outFileName)
  {
    mOutFileName = outFileName;
  }

  void aw.Saving.IImageSavingCallback.imageSaving(ImageSavingArgs args)
  {
    string imageFileName = `${mOutFileName} shape ${++mCount}, of type ${args.currentShape.shapeType}${Path.GetExtension(args.imageFileName)}`;

      // Below are two ways of specifying where Aspose.Words will save each part of the document.
      // 1 -  Set a filename for the output image file:
    args.imageFileName = imageFileName;

      // 2 -  Create a custom stream for the output image file:
    args.imageStream = new FileStream(base.artifactsDir + imageFileName, FileMode.create);

    expect(args.imageStream.CanWrite).toEqual(true);
    expect(args.isImageAvailable).toEqual(true);
    expect(args.keepImageStreamOpen).toEqual(false);
  }

  private int mCount;
  private readonly string mOutFileName;
}
```

### See Also

* module [Aspose.Words.Saving](../)
* class [SaveOptions](../saveoptions/)

