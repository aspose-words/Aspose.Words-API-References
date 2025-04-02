---
title: PdfSaveOptions class
linktitle: PdfSaveOptions class
articleTitle: PdfSaveOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.PdfSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.Pdf](../../Aspose.Words/saveformat/#Pdf) format"
type: docs
weight: 720
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/
---

## PdfSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.Pdf](../../Aspose.Words/saveformat/#Pdf) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [PdfSaveOptions](./) → [FixedPageSaveOptions](../fixedpagesaveoptions/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [PdfSaveOptions()](./constructor/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Pdf](../../Aspose.Words/saveformat/#Pdf) format. |

### Properties

| Name | Description |
| --- | --- |
| [additionalTextPositioning](./additionalTextPositioning/) | A flag specifying whether to write additional text positioning operators or not. |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [attachmentsEmbeddingMode](./attachmentsEmbeddingMode/) | Gets or sets a value determining how attachments are embedded to the PDF document. |
| [cacheBackgroundGraphics](./cacheBackgroundGraphics/) | Gets or sets a value determining whether or not to cache graphics placed in document's background. |
| [colorMode](../fixedpagesaveoptions/colorMode/) | Gets or sets a value determining how colors are rendered.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [compliance](./compliance/) | Specifies the PDF standards compliance level for output documents. |
| [createNoteHyperlinks](./createNoteHyperlinks/) | Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is ``False``. |
| [customPropertiesExport](./customPropertiesExport/) | Gets or sets a value determining the way [Document.customDocumentProperties](../../Aspose.Words/document/customDocumentProperties/) are exported to PDF file. |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [digitalSignatureDetails](./digitalSignatureDetails/) | Gets or sets the details for signing the output PDF document. |
| [displayDocTitle](./displayDocTitle/) | A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary. |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](./dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered. |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [downsampleOptions](./downsampleOptions/) | Allows to specify downsample options. |
| [embedFullFonts](./embedFullFonts/) | Controls how fonts are embedded into the resulting PDF documents. |
| [encryptionDetails](./encryptionDetails/) | Gets or sets the details for encrypting the output PDF document. |
| [exportDocumentStructure](./exportDocumentStructure/) | Gets or sets a value determining whether or not to export document structure. |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportLanguageToSpanTag](./exportLanguageToSpanTag/) | Gets or sets a value determining whether or not to create a "Span" tag in the document structure to export the text language. |
| [exportParagraphGraphicsToArtifact](./exportParagraphGraphicsToArtifact/) | Gets or sets a value determining whether a paragraph graphic should be marked as an artifact. |
| [fontEmbeddingMode](./fontEmbeddingMode/) | Specifies the font embedding mode. |
| [headerFooterBookmarksExportMode](./headerFooterBookmarksExportMode/) | Determines how bookmarks in headers/footers are exported. |
| [imageColorSpaceExportMode](./imageColorSpaceExportMode/) | Specifies how the color space will be selected for the images in PDF document. |
| [imageCompression](./imageCompression/) | Specifies compression type to be used for all images in the document. |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [interpolateImages](./interpolateImages/) | A flag indicating whether image interpolation shall be performed by a conforming reader. When ``False`` is specified, the flag is not written to the output document and the default behaviour of reader is used instead. |
| [jpegQuality](./jpegQuality/) | Gets or sets a value determining the quality of the JPEG images inside PDF document. |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafileRenderingOptions](../fixedpagesaveoptions/metafileRenderingOptions/) | Allows to specify metafile rendering options.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [numeralFormat](../fixedpagesaveoptions/numeralFormat/) | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [openHyperlinksInNewWindow](./openHyperlinksInNewWindow/) | Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |
| [optimizeOutput](../fixedpagesaveoptions/optimizeOutput/) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to ``True``.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [outlineOptions](./outlineOptions/) | Allows to specify outline options. |
| [pageLayout](./pageLayout/) | Specifies the page layout to be used when the document is opened in a PDF reader. |
| [pageMode](./pageMode/) | Specifies how the PDF document should be displayed when opened in a PDF reader. |
| [pageSavingCallback](../fixedpagesaveoptions/pageSavingCallback/) | Allows to control how separate pages are saved when a document is exported to fixed page format.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [pageSet](../fixedpagesaveoptions/pageSet/) | Gets or sets the pages to render. Default is all the pages in the document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [preblendImages](./preblendImages/) | Gets or sets a value determining whether or not to preblend transparent images with black background color. |
| [preserveFormFields](./preserveFormFields/) | Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is ``False``. |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [renderChoiceFormFieldBorder](./renderChoiceFormFieldBorder/) | Specifies whether to render PDF choice form field border. |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.Pdf](../../Aspose.Words/saveformat/#Pdf). |
| [tempFolder](../saveoptions/tempFolder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [textCompression](./textCompression/) | Specifies compression type to be used for all textual content in the document. |
| [updateAmbiguousTextFont](../saveoptions/updateAmbiguousTextFont/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateCreatedTimeProperty](../saveoptions/updateCreatedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../Aspose.Words.Properties/builtindocumentproperties/createdTime/) property is updated before saving. Default value is ``False``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateFields](../saveoptions/updateFields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastPrintedProperty](../saveoptions/updateLastPrintedProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../Aspose.Words.Properties/builtindocumentproperties/lastPrinted/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastSavedTimeProperty](../saveoptions/updateLastSavedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../Aspose.Words.Properties/builtindocumentproperties/lastSavedTime/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useAntiAliasing](../saveoptions/useAntiAliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useBookFoldPrintingSettings](./useBookFoldPrintingSettings/) | Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiplePages](../../Aspose.Words/pagesetup/multiplePages/). |
| [useCoreFonts](./useCoreFonts/) | Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |
| [useHighQualityRendering](../saveoptions/useHighQualityRendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useSdtTagAsFormFieldName](./useSdtTagAsFormFieldName/) | Specifies whether to use SDT control Tag or Id property as a name of form field in PDF. |
| [zoomBehavior](./zoomBehavior/) | Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. |
| [zoomFactor](./zoomFactor/) | Gets or sets a value determining zoom factor (in percentages) for a document. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Creates a deep clone of this object. |
|[ createSaveOptions(saveFormat)](../saveoptions/createSaveOptions/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ createSaveOptions(fileName)](../saveoptions/createSaveOptions/#string) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert headings of levels 1 to 5.
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;

expect(builder.paragraphFormat.isHeading).toEqual(true);

builder.writeln("Heading 1");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading2;

builder.writeln("Heading 1.1");
builder.writeln("Heading 1.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading3;

builder.writeln("Heading 1.2.1");
builder.writeln("Heading 1.2.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading4;

builder.writeln("Heading 1.2.2.1");
builder.writeln("Heading 1.2.2.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading5;

builder.writeln("Heading 1.2.2.2.1");
builder.writeln("Heading 1.2.2.2.2");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
options.outlineOptions.headingsOutlineLevels = 4;

// If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
// an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
// In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
// the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
// In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
// Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
// and collapse all level and 3 and higher entries when we open the document.
options.outlineOptions.expandedOutlineLevels = 2;

doc.save(base.artifactsDir + "PdfSaveOptions.expandedOutlineLevels.pdf", options);
```

Shows how to apply text compression when saving a document to PDF.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

for (let i = 0; i < 100; i++)
  builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
          "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Set the "TextCompression" property to "PdfTextCompression.None" to not apply any
// compression to text when we save the document to PDF.
// Set the "TextCompression" property to "PdfTextCompression.Flate" to apply ZIP compression
// to text when we save the document to PDF. The larger the document, the bigger the impact that this will have.
options.textCompression = pdfTextCompression;

doc.save(base.artifactsDir + "PdfSaveOptions.textCompression.pdf", options);
```

Shows how to change image color with saving options property.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
// The size of the output document may be larger with this setting.
// Set the "ColorMode" property to "Normal" to render all images in color.
let pdfSaveOptions = new aw.Saving.PdfSaveOptions();
pdfSaveOptions.colorMode = colorMode;

doc.save(base.artifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../)
* class [FixedPageSaveOptions](../fixedpagesaveoptions/)

