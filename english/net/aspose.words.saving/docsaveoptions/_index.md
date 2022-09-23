---
title: DocSaveOptions
second_title: Aspose.Words for .NET API Reference
description: Can be used to specify additional options when saving a document into the Doc or Dot format.
type: docs
weight: 4670
url: /net/aspose.words.saving/docsaveoptions/
---
## DocSaveOptions class

Can be used to specify additional options when saving a document into the Doc or Dot format.

```csharp
public class DocSaveOptions : SaveOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [DocSaveOptions](docsaveoptions/#constructor)() | Initializes a new instance of this class that can be used to save a document in the Doc format. |
| [DocSaveOptions](docsaveoptions/#constructor_1)(SaveFormat) | Initializes a new instance of this class that can be used to save a document in the Doc or Dot format. |

## Properties

| Name | Description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [AlwaysCompressMetafiles](../../aspose.words.saving/docsaveoptions/alwayscompressmetafiles/) { get; set; } | When `false`, small metafiles are not compressed for performance reason. Default value is **true**, all metafiles are compressed regardless of its size. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Gets or sets custom local time zone used for date/time fields. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Gets or sets path to default template (including filename). Default value for this property is **empty string** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Gets or sets a value determining how 3D effects are rendered. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Gets or sets a value determining how DrawingML effects are rendered. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Gets or sets a value determining how DrawingML shapes are rendered. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | When true, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [Password](../../aspose.words.saving/docsaveoptions/password/) { get; set; } | Gets/sets a password to encrypt document using RC4 encryption method. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | When `true`, pretty formats output where applicable. Default value is **false**. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Called during saving a document and accepts data about saving progress. |
| override [SaveFormat](../../aspose.words.saving/docsaveoptions/saveformat/) { get; set; } | Specifies the format in which the document will be saved if this save options object is used. Can be Doc or Dot. |
| [SavePictureBullet](../../aspose.words.saving/docsaveoptions/savepicturebullet/) { get; set; } | When `false`, PictureBullet data is not saved to output document. Default value is **true**. |
| [SaveRoutingSlip](../../aspose.words.saving/docsaveoptions/saveroutingslip/) { get; set; } | When `false`, RoutingSlip data is not saved to output document. Default value is **true**. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is `null` and no temporary files are used. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Gets or sets a value determining whether the [`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) property is updated before saving. Default value is false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Gets or sets a value determining whether the [`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) property is updated before saving. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Gets or sets a value determining whether the [`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) property is updated before saving. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Gets or sets value determining whether content of [`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) is updated before saving. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |

## Remarks

At the moment provides only the [`SaveFormat`](./saveformat/) property, but in the future will have other options added, such as an encryption password or digital signature settings.

## Examples

Shows how to set save options for older Microsoft Word formats.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Set a password which will protect the loading of the document by Microsoft Word or Aspose.Words.
// Note that this does not encrypt the contents of the document in any way.
options.Password = "MyPassword";

// If the document contains a routing slip, we can preserve it while saving by setting this flag to true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// To be able to load the document,
// we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### See Also

* class [SaveOptions](../saveoptions/)
* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
