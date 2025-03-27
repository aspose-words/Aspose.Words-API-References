---
title: RtfSaveOptions class
linktitle: RtfSaveOptions class
articleTitle: RtfSaveOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.RtfSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.Rtf](../../Aspose.Words/saveformat/#Rtf) format"
type: docs
weight: 770
url: /nodejs-net/Aspose.Words.Saving/rtfsaveoptions/
---

## RtfSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.Rtf](../../Aspose.Words/saveformat/#Rtf) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [RtfSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [RtfSaveOptions()](./RtfSaveOptions/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportCompactSize](./exportCompactSize/) | Allows to make output RTF documents smaller in size, but if they contain  RTL (right-to-left) text, it will not be displayed correctly. |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportImagesForOldReaders](./exportImagesForOldReaders/) | Specifies whether the keywords for "old readers" are written to RTF or not. This can significantly affect the size of the RTF document. |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.Rtf](../../Aspose.Words/saveformat/#Rtf). |
| [saveImagesAsWmf](./saveImagesAsWmf/) | When ``True`` all images will be saved as WMF. |
| [tempFolder](../saveoptions/tempFolder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateAmbiguousTextFont](../saveoptions/updateAmbiguousTextFont/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateCreatedTimeProperty](../saveoptions/updateCreatedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../Aspose.Words.Properties/builtindocumentproperties/createdTime/) property is updated before saving. Default value is ``False``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateFields](../saveoptions/updateFields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastPrintedProperty](../saveoptions/updateLastPrintedProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../Aspose.Words.Properties/builtindocumentproperties/lastPrinted/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastSavedTimeProperty](../saveoptions/updateLastSavedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../Aspose.Words.Properties/builtindocumentproperties/lastSavedTime/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useAntiAliasing](../saveoptions/useAntiAliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useHighQualityRendering](../saveoptions/useHighQualityRendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Methods

| Name | Description |
| --- | --- |
|[ createSaveOptions(saveFormat)](../saveoptions/createSaveOptions/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ createSaveOptions(fileName)](../saveoptions/createSaveOptions/#string) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Examples

Shows how to save a document to .rtf with custom options.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// Create an "RtfSaveOptions" object to pass to the document's "Save" method to modify how we save it to an RTF.
let options = new aw.Saving.RtfSaveOptions();

expect(options.saveFormat).toEqual(aw.SaveFormat.Rtf);

// Set the "ExportCompactSize" property to "true" to
// reduce the saved document's size at the cost of right-to-left text compatibility.
options.exportCompactSize = true;

// Set the "ExportImagesFotOldReaders" property to "true" to use extra keywords to ensure that our document is
// compatible with pre-Microsoft Word 97 readers and WordPad.
// Set the "ExportImagesFotOldReaders" property to "false" to reduce the size of the document,
// but prevent old readers from being able to read any non-metafile or BMP images that the document may contain.
options.exportImagesForOldReaders = exportImagesForOldReaders;

doc.save(base.artifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### See Also

* module [Aspose.Words.Saving](../)
* class [SaveOptions](../saveoptions/)

