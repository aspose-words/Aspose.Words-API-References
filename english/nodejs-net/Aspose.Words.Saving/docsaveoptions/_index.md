---
title: DocSaveOptions class
linktitle: DocSaveOptions class
articleTitle: DocSaveOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.DocSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.Doc](../../aspose.words/saveformat/#Doc) or [SaveFormat.Dot](../../aspose.words/saveformat/#Dot) format"
type: docs
weight: 100
url: /nodejs-net/aspose.words.saving/docsaveoptions/
---

## DocSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.Doc](../../aspose.words/saveformat/#Doc) or
[SaveFormat.Dot](../../aspose.words/saveformat/#Dot) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




### Remarks

At the moment provides only the [DocSaveOptions.saveFormat](./saveFormat/) property, but in the future will have
other options added, such as an encryption password or digital signature settings.




**Inheritance:** [DocSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [DocSaveOptions()](./constructor/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Doc](../../aspose.words/saveformat/#Doc) format. |
| [DocSaveOptions(saveFormat)](./constructor/#saveformat) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Doc](../../aspose.words/saveformat/#Doc) or [SaveFormat.Dot](../../aspose.words/saveformat/#Dot) format. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [alwaysCompressMetafiles](./alwaysCompressMetafiles/) | When ``false``, small metafiles are not compressed for performance reason. Default value is ``true``, all metafiles are compressed regardless of its size. |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** .<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [digitalSignatureDetails](./digitalSignatureDetails/) | Gets or sets [DigitalSignatureDetails](../digitalsignaturedetails/) object used to sign a document. |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``true``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [password](./password/) | Gets/sets a password to encrypt document using RC4 encryption method. |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``true``, pretty formats output where applicable. Default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can be [SaveFormat.Doc](../../aspose.words/saveformat/#Doc) or [SaveFormat.Dot](../../aspose.words/saveformat/#Dot). |
| [savePictureBullet](./savePictureBullet/) | When ``false``, PictureBullet data is not saved to output document. Default value is ``true``. |
| [saveRoutingSlip](./saveRoutingSlip/) | When ``false``, RoutingSlip data is not saved to output document. Default value is ``true``. |
| [tempFolder](../saveoptions/tempFolder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default, this property is ``null`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateAmbiguousTextFont](../saveoptions/updateAmbiguousTextFont/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateCreatedTimeProperty](../saveoptions/updateCreatedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../aspose.words.properties/builtindocumentproperties/createdTime/) property is updated before saving. Default value is ``false``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateFields](../saveoptions/updateFields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastPrintedProperty](../saveoptions/updateLastPrintedProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../aspose.words.properties/builtindocumentproperties/lastPrinted/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastSavedTimeProperty](../saveoptions/updateLastSavedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../aspose.words.properties/builtindocumentproperties/lastSavedTime/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateOleControlImages](../saveoptions/updateOleControlImages/) | Gets or sets a value determining whether OLE controls presentation image will be updated.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useAntiAliasing](../saveoptions/useAntiAliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useHighQualityRendering](../saveoptions/useHighQualityRendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Methods

| Name | Description |
| --- | --- |
|[ createSaveOptions(saveFormat)](../saveoptions/createSaveOptions/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ createSaveOptions(fileName)](../saveoptions/createSaveOptions/#string) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Examples

Shows how to set save options for older Microsoft Word formats.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.write("Hello world!");

let options = new aw.Saving.DocSaveOptions(aw.SaveFormat.Doc);

// Set a password which will protect the loading of the document by Microsoft Word or Aspose.words.
// Note that this does not encrypt the contents of the document in any way.
options.password = "MyPassword";

// If the document contains a routing slip, we can preserve it while saving by setting this flag to true.
options.saveRoutingSlip = true;

doc.save(base.artifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// To be able to load the document,
// we will need to apply the password we specified in the DocSaveOptions object in a LoadOptions object.
expect(() => doc = new aw.Document(base.artifactsDir + "DocSaveOptions.SaveAsDoc.doc")).toThrow("The document password is incorrect.");

let loadOptions = new aw.Loading.LoadOptions("MyPassword");
doc = new aw.Document(base.artifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

expect(doc.getText().trim()).toEqual("Hello world!");
```

### See Also

* module [Aspose.Words.Saving](../)
* class [SaveOptions](../saveoptions/)

