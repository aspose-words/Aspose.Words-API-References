---
title: "PdfSaveOptions"
second_title: Aspose.Words for .NET API Reference
description: ""
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

| Name | Description |
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

### Examples

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

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* namespace [Aspose.Words.Saving](../../aspose.words.saving)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
