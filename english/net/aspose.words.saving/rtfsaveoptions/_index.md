---
title: RtfSaveOptions Class
linktitle: RtfSaveOptions
articleTitle: RtfSaveOptions
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Saving.RtfSaveOptions class. Can be used to specify additional options when saving a document into the Rtf format in C#.
type: docs
weight: 5480
url: /net/aspose.words.saving/rtfsaveoptions/
---
## RtfSaveOptions class

Can be used to specify additional options when saving a document into the Rtf format.

To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/net/specify-save-options/) documentation article.

```csharp
public class RtfSaveOptions : SaveOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [RtfSaveOptions](rtfsaveoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is `false`. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Gets or sets custom local time zone used for date/time fields. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Gets or sets path to default template (including filename). Default value for this property is **empty string** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Gets or sets a value determining how 3D effects are rendered. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Gets or sets a value determining how DrawingML effects are rendered. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Gets or sets a value determining how DrawingML shapes are rendered. |
| [ExportCompactSize](../../aspose.words.saving/rtfsaveoptions/exportcompactsize/) { get; set; } | Allows to make output RTF documents smaller in size, but if they contain RTL (right-to-left) text, it will not be displayed correctly. Default value is `false`. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | When `true`, causes the name and version of Aspose.Words to be embedded into produced files. Default value is `true`. |
| [ExportImagesForOldReaders](../../aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/) { get; set; } | Specifies whether the keywords for "old readers" are written to RTF or not. This can significantly affect the size of the RTF document. Default value is `true`. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is `false`. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | When `true`, pretty formats output where applicable. Default value is `false`. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Called during saving a document and accepts data about saving progress. |
| override [SaveFormat](../../aspose.words.saving/rtfsaveoptions/saveformat/) { get; set; } | Specifies the format in which the document will be saved if this save options object is used. Can only be Rtf. |
| [SaveImagesAsWmf](../../aspose.words.saving/rtfsaveoptions/saveimagesaswmf/) { get; set; } | When `true` all images will be saved as WMF. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is `null` and no temporary files are used. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Gets or sets a value determining whether the [`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) property is updated before saving. Default value is `false`; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is `true`. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Gets or sets a value determining whether the [`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) property is updated before saving. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Gets or sets a value determining whether the [`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) property is updated before saving. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |

## Examples

Shows how to save a document to .rtf with custom options.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Create an "RtfSaveOptions" object to pass to the document's "Save" method to modify how we save it to an RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Set the "ExportCompactSize" property to "true" to
// reduce the saved document's size at the cost of right-to-left text compatibility.
options.ExportCompactSize = true;

// Set the "ExportImagesFotOldReaders" property to "true" to use extra keywords to ensure that our document is
// compatible with pre-Microsoft Word 97 readers and WordPad.
// Set the "ExportImagesFotOldReaders" property to "false" to reduce the size of the document,
// but prevent old readers from being able to read any non-metafile or BMP images that the document may contain.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### See Also

* class [SaveOptions](../saveoptions/)
* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
