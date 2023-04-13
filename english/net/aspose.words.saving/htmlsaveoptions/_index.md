---
title: HtmlSaveOptions Class
linktitle: HtmlSaveOptions
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Saving.HtmlSaveOptions class. Can be used to specify additional options when saving a document into the Html Mhtml Epub Azw3 or Mobi format in C#.
type: docs
weight: 4930
url: /net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Can be used to specify additional options when saving a document into the Html, Mhtml, Epub, Azw3 or Mobi format.

To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/net/specify-save-options/) documentation article.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | Initializes a new instance of this class that can be used to save a document in the Html format. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Initializes a new instance of this class that can be used to save a document in the Html, Mhtml, Epub, Azw3 or Mobi format. |

## Properties

| Name | Description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is `false`. |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is `false`. |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is Inline for HTML/MHTML and External for EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Gets or sets custom local time zone used for date/time fields. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Gets or sets path to default template (including filename). Default value for this property is **empty string** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Gets or sets a value determining how 3D effects are rendered. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Gets or sets a value determining how DrawingML effects are rendered. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Gets or sets a value determining how DrawingML shapes are rendered. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | Specifies how the document should be split when saving to Html, Epub or Azw3 format. Default is None for HTML and HeadingParagraph for EPUB and AZW3. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | Specifies the maximum level of headings at which to split the document. Default value is `2`. |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | Specifies the encoding to use when exporting to HTML, MHTML or EPUB. Default value is `new UTF8Encoding(false)` (UTF-8 without BOM). |
| [EpubNavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/) { get; set; } | Specifies the maximum level of headings populated to the navigation map when exporting to IDPF EPUB or AZW3 formats. Default value is `3`. |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is `false`. |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is `false`. |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | Controls how drop-down form fields are saved to HTML or MHTML. Default value is `false`. |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is `false`. |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is `false`. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | When `true`, causes the name and version of Aspose.Words to be embedded into produced files. Default value is `true`. |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is PerSection for HTML/MHTML and None for EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is `false`. |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | Specifies whether language information is exported to HTML, MHTML or EPUB. Default is `false`. |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | Controls how list labels are output to HTML, MHTML or EPUB. Default value is Auto. |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | Specifies whether original URL should be used as the URL of the linked images. Default value is `false`. |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is `false`. |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is `false`. |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is `false`. |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is `true` for HTML and `false` for MHTML and EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | Controls whether [`Shape`](../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is `false`. |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | Controls how text input form fields are saved to HTML or MHTML. Default value is `false`. |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is `false`. |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When `true`, writes a DOCTYPE declaration in the document prior to the root element. Default value is `false`. When saving to EPUB or HTML5 (Html5) the DOCTYPE declaration is always written. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is `0`. |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is Xhtml. |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is `96 dpi`. |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is `false`. |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is Png, meaning that metafiles are rendered to raster PNG images. |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is Image. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | When `true`, pretty formats output where applicable. Default value is `false`. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Called during saving a document and accepts data about saving progress. |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | Specifies whether font family names used in the document are resolved and substituted according to [`FontSettings`](../../aspose.words/document/fontsettings/) when being written into HTML-based formats. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | Specifies the format in which the document will be saved if this save options object is used. Can be Html, Mhtml, Epub, Azw3 or Mobi. |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is `true`. |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is All. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is `null` and no temporary files are used. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Gets or sets a value determining whether the [`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) property is updated before saving. Default value is `false`; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is `true`. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Gets or sets a value determining whether the [`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) property is updated before saving. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Gets or sets a value determining whether the [`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) property is updated before saving. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |

## Examples

Shows how to specify the folder for storing linked images after saving to .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Set an option to export form fields as plain text instead of HTML input elements.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Shows how to use a specific encoding when saving a document to .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Use a SaveOptions object to specify the encoding for a document that we will save.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// By default, an output .epub document will have all its contents in one HTML part.
// A split criterion allows us to segment the document into several HTML parts.
// We will set the criteria to split the document into heading paragraphs.
// This is useful for readers who cannot read HTML files more significant than a specific size.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Specify that we want to export document properties.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Shows how to split a document into parts and save them.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
    // to modify how we convert the document to HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // If we save the document normally, there will be one output HTML
    // document with all the source document's contents.
    // Set the "DocumentSplitCriteria" property to "DocumentSplitCriteria.SectionBreak" to
    // save our document to multiple HTML files: one for each section.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Assign a custom callback to the "DocumentPartSavingCallback" property to alter the document part saving logic.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // If we convert a document that contains images into html, we will end up with one html file which links to several images.
    // Each image will be in the form of a file in the local file system.
    // There is also a callback that can customize the name and file system location of each image.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

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

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // We can access the entire source document via the "Document" property.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // Below are two ways of specifying where Aspose.Words will save each part of the document.
        // 1 -  Set a filename for the output part file:
        args.DocumentPartFileName = partFileName;

        // 2 -  Create a custom stream for the output part file:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
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

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // Below are two ways of specifying where Aspose.Words will save each part of the document.
        // 1 -  Set a filename for the output image file:
        args.ImageFileName = imageFileName;

        // 2 -  Create a custom stream for the output image file:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### See Also

* class [SaveOptions](../saveoptions/)
* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
