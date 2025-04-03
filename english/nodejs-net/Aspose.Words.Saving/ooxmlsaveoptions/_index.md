---
title: OoxmlSaveOptions class
linktitle: OoxmlSaveOptions class
articleTitle: OoxmlSaveOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.OoxmlSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.Docx](../../aspose.words/saveformat/#Docx), [SaveFormat.Docm](../../aspose.words/saveformat/#Docm), [SaveFormat.Dotx](../../aspose.words/saveformat/#Dotx), [SaveFormat.Dotm](../../aspose.words/saveformat/#Dotm) or [SaveFormat.FlatOpc](../../aspose.words/saveformat/#FlatOpc) format"
type: docs
weight: 530
url: /nodejs-net/Aspose.Words.Saving/ooxmlsaveoptions/
---

## OoxmlSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.Docx](../../aspose.words/saveformat/#Docx),
[SaveFormat.Docm](../../aspose.words/saveformat/#Docm), [SaveFormat.Dotx](../../aspose.words/saveformat/#Dotx), [SaveFormat.Dotm](../../aspose.words/saveformat/#Dotm) or
[SaveFormat.FlatOpc](../../aspose.words/saveformat/#FlatOpc) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [OoxmlSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [OoxmlSaveOptions()](./constructor/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Docx](../../aspose.words/saveformat/#Docx) format. |
| [OoxmlSaveOptions(saveFormat)](./constructor/#saveformat) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Docx](../../aspose.words/saveformat/#Docx), [SaveFormat.Docm](../../aspose.words/saveformat/#Docm), [SaveFormat.Dotx](../../aspose.words/saveformat/#Dotx), [SaveFormat.Dotm](../../aspose.words/saveformat/#Dotm) or [SaveFormat.FlatOpc](../../aspose.words/saveformat/#FlatOpc) format. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [compliance](./compliance/) | Specifies the OOXML version for the output document. The default value is [OoxmlCompliance.Ecma376_2006](../ooxmlcompliance/#Ecma376_2006). |
| [compressionLevel](./compressionLevel/) | Specifies the compression level used to save document. The default value is [CompressionLevel.Normal](../compressionlevel/#Normal). |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [digitalSignatureDetails](./digitalSignatureDetails/) | Gets or sets [DigitalSignatureDetails](../digitalsignaturedetails/) object used to sign a document. |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [keepLegacyControlChars](./keepLegacyControlChars/) | Keeps original representation of legacy control characters. |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [password](./password/) | Gets/sets a password to encrypt document using ECMA376 Standard encryption algorithm. |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.Docx](../../aspose.words/saveformat/#Docx), [SaveFormat.Docm](../../aspose.words/saveformat/#Docm), [SaveFormat.Dotx](../../aspose.words/saveformat/#Dotx), [SaveFormat.Dotm](../../aspose.words/saveformat/#Dotm) or [SaveFormat.FlatOpc](../../aspose.words/saveformat/#FlatOpc). |
| [tempFolder](../saveoptions/tempFolder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateAmbiguousTextFont](../saveoptions/updateAmbiguousTextFont/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateCreatedTimeProperty](../saveoptions/updateCreatedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../aspose.words.properties/builtindocumentproperties/createdTime/) property is updated before saving. Default value is ``False``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateFields](../saveoptions/updateFields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastPrintedProperty](../saveoptions/updateLastPrintedProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../aspose.words.properties/builtindocumentproperties/lastPrinted/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastSavedTimeProperty](../saveoptions/updateLastSavedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../aspose.words.properties/builtindocumentproperties/lastSavedTime/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useAntiAliasing](../saveoptions/useAntiAliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useHighQualityRendering](../saveoptions/useHighQualityRendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [zip64Mode](./zip64Mode/) | Specifies whether or not to use ZIP64 format extensions for the output document. The default value is [Zip64Mode.Never](../zip64mode/#Never). |

### Methods

| Name | Description |
| --- | --- |
|[ createSaveOptions(saveFormat)](../saveoptions/createSaveOptions/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ createSaveOptions(fileName)](../saveoptions/createSaveOptions/#string) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Examples

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// If we configure compatibility options to comply with Microsoft Word 2003,
// inserting an image will define its shape using VML.
doc.compatibilityOptions.optimizeFor(aw.Settings.MsWordVersion.Word2003);
builder.insertImage(base.imageDir + "Transparent background logo.png");

expect(doc.getShape(0, true).markupLanguage).toEqual(aw.Drawing.ShapeMarkupLanguage.Vml);

// The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
// If we set the "Compliance" property of the SaveOptions object to "OoxmlCompliance.Iso29500_2008_Strict",
// any document we save while passing this object will have to follow that standard. 
let saveOptions = new aw.Saving.OoxmlSaveOptions();
saveOptions.compliance = aw.Saving.OoxmlCompliance.Iso29500_2008_Strict;
saveOptions.saveFormat = aw.SaveFormat.Docx;

doc.save(base.artifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
doc = new aw.Document(base.artifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

expect(doc.getShape(0, true).markupLanguage).toEqual(aw.Drawing.ShapeMarkupLanguage.Dml);
```

### See Also

* module [Aspose.Words.Saving](../)
* class [SaveOptions](../saveoptions/)

