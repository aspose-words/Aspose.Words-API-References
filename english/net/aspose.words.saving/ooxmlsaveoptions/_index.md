---
title: OoxmlSaveOptions
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 5020
url: /net/aspose.words.saving/ooxmlsaveoptions/
---
## OoxmlSaveOptions class

Can be used to specify additional options when saving a document into the Docx, Docm, Dotx, Dotm or FlatOpc format.

```csharp
public class OoxmlSaveOptions : SaveOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [OoxmlSaveOptions](ooxmlsaveoptions)() | Initializes a new instance of this class that can be used to save a document in the Docx format. |
| [OoxmlSaveOptions](ooxmlsaveoptions)(SaveFormat) | Initializes a new instance of this class that can be used to save a document in the Docx, Docm, Dotx, Dotm or FlatOpc format. |

## Properties

| Name | Description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [Compliance](../../aspose.words.saving/ooxmlsaveoptions/compliance) { get; set; } | Specifies the OOXML version for the output document. The default value is Ecma376_2006. |
| [CompressionLevel](../../aspose.words.saving/ooxmlsaveoptions/compressionlevel) { get; set; } | Specifies the compression level used to save document. The default value is Normal. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Gets or sets custom local time zone used for date/time fields. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Gets or sets path to default template (including filename). Default value for this property is **empty string** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Gets or sets a value determining how 3D effects are rendered. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Gets or sets a value determining how DrawingML effects are rendered. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Gets or sets a value determining how DrawingML shapes are rendered. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | When true, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Gets or sets value determining which document formats are allowed to be mapped by [`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping). By default only FlatOpc document format is allowed to be mapped. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [KeepLegacyControlChars](../../aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars) { get; set; } | Keeps original representation of legacy control characters. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [Password](../../aspose.words.saving/ooxmlsaveoptions/password) { get; set; } | Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | When `true`, pretty formats output where applicable. Default value is **false**. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Called during saving a document and accepts data about saving progress. |
| override [SaveFormat](../../aspose.words.saving/ooxmlsaveoptions/saveformat) { get; set; } | Specifies the format in which the document will be saved if this save options object is used. Can be Docx, Docm, Dotx, Dotm or FlatOpc. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is `null` and no temporary files are used. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Gets or sets a value determining whether the [`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) property is updated before saving. Default value is false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Gets or sets a value determining whether the [`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) property is updated before saving. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Gets or sets a value determining whether the [`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) property is updated before saving. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Gets or sets value determining whether content of [`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) is updated before saving. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |

### Examples

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// If we configure compatibility options to comply with Microsoft Word 2003,
// inserting an image will define its shape using VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
// If we set the "Compliance" property of the SaveOptions object to "OoxmlCompliance.Iso29500_2008_Strict",
// any document we save while passing this object will have to follow that standard. 
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### See Also

* class [SaveOptions](../saveoptions)
* namespace [Aspose.Words.Saving](../../aspose.words.saving)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
