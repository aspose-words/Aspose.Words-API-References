---
title: XamlFlowSaveOptions class
linktitle: XamlFlowSaveOptions class
articleTitle: XamlFlowSaveOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.XamlFlowSaveOptions class. Can be used to specify additional options when saving a document into the  [SaveFormat.XamlFlow](../../aspose.words/saveformat/#XamlFlow) or [SaveFormat.XamlFlowPack](../../aspose.words/saveformat/#XamlFlowPack) format"
type: docs
weight: 920
url: /nodejs-net/aspose.words.saving/xamlflowsaveoptions/
---

## XamlFlowSaveOptions class

Can be used to specify additional options when saving a document into the 
[SaveFormat.XamlFlow](../../aspose.words/saveformat/#XamlFlow) or [SaveFormat.XamlFlowPack](../../aspose.words/saveformat/#XamlFlowPack) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [XamlFlowSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [XamlFlowSaveOptions()](./constructor/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XamlFlow](../../aspose.words/saveformat/#XamlFlow) format. |
| [XamlFlowSaveOptions(saveFormat)](./constructor/#saveformat) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XamlFlow](../../aspose.words/saveformat/#XamlFlow) or [SaveFormat.XamlFlowPack](../../aspose.words/saveformat/#XamlFlowPack) format. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** .<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``true``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [imageSavingCallback](./imageSavingCallback/) | Allows to control how images are saved when a document is saved to XAML. |
| [imagesFolder](./imagesFolder/) | Specifies the physical folder where images are saved when exporting a document to XAML format. Default is an empty string. |
| [imagesFolderAlias](./imagesFolderAlias/) | Specifies the name of the folder used to construct image URIs written into an XAML document. Default is an empty string. |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``true``, pretty formats output where applicable. Default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [replaceBackslashWithYenSign](./replaceBackslashWithYenSign/) | Specifies whether backslash characters should be replaced with yen signs. Default value is ``false``. |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XamlFlow](../../aspose.words/saveformat/#XamlFlow). |
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

### See Also

* module [Aspose.Words.Saving](../)
* class [SaveOptions](../saveoptions/)

