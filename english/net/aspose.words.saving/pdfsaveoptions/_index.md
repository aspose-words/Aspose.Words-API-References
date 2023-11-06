---
title: PdfSaveOptions Class
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.PdfSaveOptions class. Can be used to specify additional options when saving a document into the Pdf format in C#.
type: docs
weight: 5530
url: /net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Can be used to specify additional options when saving a document into the Pdf format.

To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/net/specify-save-options/) documentation article.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | Initializes a new instance of this class that can be used to save a document in the Pdf format. |

## Properties

| Name | Description |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | A flag specifying whether to write additional text positioning operators or not. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is `false`. |
| [CacheBackgroundGraphics](../../aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/) { get; set; } | Gets or sets a value determining whether or not to cache graphics placed in document's background. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Gets or sets a value determining how colors are rendered. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | Specifies the PDF standards compliance level for output documents. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is `false`. |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | Gets or sets a value determining the way [`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) are exported to PDF file. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Gets or sets custom local time zone used for date/time fields. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Gets or sets path to default template (including filename). Default value for this property is **empty string** (Empty). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | Gets or sets the details for signing the output PDF document. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Gets or sets a value determining how 3D effects are rendered. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | Gets or sets a value determining how DrawingML effects are rendered. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Gets or sets a value determining how DrawingML shapes are rendered. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | Allows to specify downsample options. |
| [EmbedAttachments](../../aspose.words.saving/pdfsaveoptions/embedattachments/) { get; set; } | Gets or sets a value determining whether or not to embed attachments to the PDF document. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | Controls how fonts are embedded into the resulting PDF documents. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | Gets or sets the details for encrypting the output PDF document. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | Gets or sets a value determining whether or not to export document structure. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | When `true`, causes the name and version of Aspose.Words to be embedded into produced files. Default value is `true`. |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | Gets or sets a value determining whether or not to create a "Span" tag in the document structure to export the text language. |
| [ExportParagraphGraphicsToArtifact](../../aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/) { get; set; } | Gets or sets a value determining whether a paragraph graphic should be marked as an artifact. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | Specifies the font embedding mode. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | Determines how bookmarks in headers/footers are exported. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | Specifies how the color space will be selected for the images in PDF document. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | Specifies compression type to be used for all images in the document. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | A flag indicating whether image interpolation shall be performed by a conforming reader. When `false` is specified, the flag is not written to the output document and the default behaviour of reader is used instead. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | Gets or sets a value determining the quality of the JPEG images inside PDF document. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is `false`. |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Allows to specify metafile rendering options. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Gets or sets [`NumeralFormat`](../numeralformat/) used for rendering of numerals. European numerals are used by default. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to `true`. Default is `false`. |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | Allows to specify outline options. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | Specifies how the PDF document should be displayed when opened in the PDF reader. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Gets or sets the pages to render. Default is all the pages in the document. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | Gets or sets a value determining whether or not to preblend transparent images with black background color. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is `false`. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | When `true`, pretty formats output where applicable. Default value is `false`. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Called during saving a document and accepts data about saving progress. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | Specifies the format in which the document will be saved if this save options object is used. Can only be Pdf. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is `null` and no temporary files are used. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | Specifies compression type to be used for all textual content in the document. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Gets or sets a value determining whether the [`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) property is updated before saving. Default value is `false`; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is `true`. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Gets or sets a value determining whether the [`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) property is updated before saving. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Gets or sets a value determining whether the [`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) property is updated before saving. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [`MultiplePages`](../../aspose.words/pagesetup/multiplepages/). |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior/) { get; set; } | Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor/) { get; set; } | Gets or sets a value determining zoom factor (in percentages) for a document. |

## Methods

| Name | Description |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone/)() | Creates a deep clone of this object. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Determines whether the specified object is equal in value to the current object. |

## Examples

Shows how to change image color with saving options property.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
// The size of the output document may be larger with this setting.
// Set the "ColorMode" property to "Normal" to render all images in color.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

Shows how to apply text compression when saving a document to PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "TextCompression" property to "PdfTextCompression.None" to not apply any
// compression to text when we save the document to PDF.
// Set the "TextCompression" property to "PdfTextCompression.Flate" to apply ZIP compression
// to text when we save the document to PDF. The larger the document, the bigger the impact that this will have.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Shows how to convert a whole document to PDF with three levels in the document outline.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert headings of levels 1 to 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
// an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
// In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
// the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
// In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
// Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
// and collapse all level and 3 and higher entries when we open the document.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### See Also

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
