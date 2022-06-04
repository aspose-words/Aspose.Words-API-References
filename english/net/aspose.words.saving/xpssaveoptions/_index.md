---
title: XpsSaveOptions
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 5380
url: /net/aspose.words.saving/xpssaveoptions/
---
## XpsSaveOptions class

Can be used to specify additional options when saving a document into the Xps format.

```csharp
public class XpsSaveOptions : FixedPageSaveOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [XpsSaveOptions](xpssaveoptions#constructor)() | Initializes a new instance of this class that can be used to save a document in the Xps format. |
| [XpsSaveOptions](xpssaveoptions#constructor_1)(SaveFormat) | Initializes a new instance of this class that can be used to save a document in the Xps or OpenXps format. |

## Properties

| Name | Description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | Gets or sets a value determining how colors are rendered. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Gets or sets custom local time zone used for date/time fields. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Gets or sets path to default template (including filename). Default value for this property is **empty string** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Gets or sets a value determining how 3D effects are rendered. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Gets or sets a value determining how DrawingML effects are rendered. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Gets or sets a value determining how DrawingML shapes are rendered. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | When true, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Gets or sets value determining which document formats are allowed to be mapped by [`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping). By default only FlatOpc document format is allowed to be mapped. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality) { get; set; } | Gets or sets a value determining the quality of the JPEG images inside Html document. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | Allows to specify metafile rendering options. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | Gets or sets [`NumeralFormat`](../numeralformat) used for rendering of numerals. European numerals are used by default. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput) { get; set; } | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to true. Default is false. |
| [OutlineOptions](../../aspose.words.saving/xpssaveoptions/outlineoptions) { get; } | Allows to specify outline options. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | Gets or sets the pages to render. Default is all the pages in the document. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | When `true`, pretty formats output where applicable. Default value is **false**. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Called during saving a document and accepts data about saving progress. |
| override [SaveFormat](../../aspose.words.saving/xpssaveoptions/saveformat) { get; set; } | Specifies the format in which the document will be saved if this save options object is used. Can only be Xps. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is `null` and no temporary files are used. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Gets or sets a value determining whether the [`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) property is updated before saving. Default value is false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Gets or sets a value determining whether the [`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) property is updated before saving. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Gets or sets a value determining whether the [`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) property is updated before saving. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Gets or sets value determining whether content of [`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) is updated before saving. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings) { get; set; } | Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [`MultiplePages`](../../aspose.words/pagesetup/multiplepages). |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |

## Methods

| Name | Description |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | Determines whether the specified object is equal in value to the current object. |

### Examples

Shows how to limit the headings' level that will appear in the outline of a saved XPS document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert headings that can serve as TOC entries of levels 1, 2, and then 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Create an "XpsSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// The output XPS document will contain an outline, a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "2" to exclude all headings whose levels are above 2 from the outline.
// The last two headings we have inserted above will not appear.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### See Also

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* namespace [Aspose.Words.Saving](../../aspose.words.saving)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
