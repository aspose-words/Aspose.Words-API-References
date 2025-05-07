---
title: OdtSaveOptions class
linktitle: OdtSaveOptions class
articleTitle: OdtSaveOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.OdtSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.Odt](../../aspose.words/saveformat/#Odt) or [SaveFormat.Ott](../../aspose.words/saveformat/#Ott) format"
type: docs
weight: 510
url: /nodejs-net/aspose.words.saving/odtsaveoptions/
---

## OdtSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.Odt](../../aspose.words/saveformat/#Odt) or
[SaveFormat.Ott](../../aspose.words/saveformat/#Ott) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




### Remarks

At the moment provides only the [OdtSaveOptions.saveFormat](./saveFormat/) property, but in the future will have
other options added, such as an encryption password or digital signature settings.




**Inheritance:** [OdtSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [OdtSaveOptions()](./constructor/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Odt](../../aspose.words/saveformat/#Odt) format. |
| [OdtSaveOptions(password)](./constructor/#string) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Odt](../../aspose.words/saveformat/#Odt) format encrypted with a password. |
| [OdtSaveOptions(saveFormat)](./constructor/#saveformat) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Odt](../../aspose.words/saveformat/#Odt) or [SaveFormat.Ott](../../aspose.words/saveformat/#Ott) format. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [digitalSignatureDetails](./digitalSignatureDetails/) | Gets or sets [DigitalSignatureDetails](../digitalsignaturedetails/) object used to sign a document. |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``true``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [isStrictSchema11](./isStrictSchema11/) | Specifies whether export should correspond to ODT specification 1.1 strictly. OOo 3.0 displays files correctly when they contain elements and attributes of ODT 1.2. Use "false" for this purpose, or "true" for strict conformity of specification 1.1. The default value is ``false``. |
| [measureUnit](./measureUnit/) | Allows to specify units of measure to apply to document content. The default value is [OdtSaveMeasureUnit.Centimeters](../odtsavemeasureunit/#Centimeters) |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [password](./password/) | Gets or sets a password to encrypt document. |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``true``, pretty formats output where applicable. Default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.Odt](../../aspose.words/saveformat/#Odt) or [SaveFormat.Ott](../../aspose.words/saveformat/#Ott). |
| [tempFolder](../saveoptions/tempFolder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``null`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateAmbiguousTextFont](../saveoptions/updateAmbiguousTextFont/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateCreatedTimeProperty](../saveoptions/updateCreatedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../aspose.words.properties/builtindocumentproperties/createdTime/) property is updated before saving. Default value is ``false``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateFields](../saveoptions/updateFields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
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

Shows how to make a saved document conform to an older ODT schema.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let saveOptions = new aw.Saving.OdtSaveOptions();
saveOptions.measureUnit = aw.Saving.OdtSaveMeasureUnit.Centimeters;
saveOptions.isStrictSchema11 = exportToOdt11Specs;

doc.save(base.artifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

Shows how to use different measurement units to define style parameters of a saved ODT document.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// When we export the document to .odt, we can use an OdtSaveOptions object to modify how we save the document.
// We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Centimeters"
// to define content such as style parameters using the metric system, which Open Office uses. 
// We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Inches"
// to define content such as style parameters using the imperial system, which Microsoft Word uses.
let saveOptions = new aw.Saving.OdtSaveOptions();
saveOptions.measureUnit = odtSaveMeasureUnit;

doc.save(base.artifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../)
* class [SaveOptions](../saveoptions/)

