---
title: SaveOptions class
linktitle: SaveOptions class
articleTitle: SaveOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.SaveOptions class. This is an abstract base class for classes that allow the user to specify additional options when saving a document into a particular format"
type: docs
weight: 780
url: /nodejs-net/Aspose.Words.Saving/saveoptions/
---

## SaveOptions class

This is an abstract base class for classes that allow the user to specify additional
options when saving a document into a particular format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




### Remarks

An instance of the [SaveOptions](./) class or any derived class is passed to the stream Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions)
or string [Document.save()](../../aspose.words/document/save/#string_saveoptions) overloads for the user to define custom options when saving a document.



### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](./allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``. |
| [defaultTemplate](./defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** (). |
| [dml3DEffectsRenderingMode](./dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered. |
| [dmlEffectsRenderingMode](./dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered. |
| [dmlRenderingMode](./dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered. |
| [exportGeneratorName](./exportGeneratorName/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``. |
| [imlRenderingMode](./imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [memoryOptimization](./memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``. |
| [prettyFormat](./prettyFormat/) | When ``True``, pretty formats output where applicable. Default value is ``False``. |
| [progressCallback](./progressCallback/) | Called during saving a document and accepts data about saving progress. |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. |
| [tempFolder](./tempFolder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used. |
| [updateAmbiguousTextFont](./updateAmbiguousTextFont/) | Determines whether the font attributes will be changed according to the character code being used. |
| [updateCreatedTimeProperty](./updateCreatedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../aspose.words.properties/builtindocumentproperties/createdTime/) property is updated before saving. Default value is ``False``; |
| [updateFields](./updateFields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``. |
| [updateLastPrintedProperty](./updateLastPrintedProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../aspose.words.properties/builtindocumentproperties/lastPrinted/) property is updated before saving. |
| [updateLastSavedTimeProperty](./updateLastSavedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../aspose.words.properties/builtindocumentproperties/lastSavedTime/) property is updated before saving. |
| [useAntiAliasing](./useAntiAliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [useHighQualityRendering](./useHighQualityRendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |

### Methods

| Name | Description |
| --- | --- |
|[ createSaveOptions(saveFormat)](./createSaveOptions/#saveformat) | Creates a save options object of a class suitable for the specified save format. |
|[ createSaveOptions(fileName)](./createSaveOptions/#string) | Creates a save options object of a class suitable for the file extension specified in the given file name. |

### Examples

Shows how to use a specific encoding when saving a document to .epub.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

// Use a SaveOptions object to specify the encoding for a document that we will save.
let saveOptions = new aw.Saving.HtmlSaveOptions();
saveOptions.saveFormat = aw.SaveFormat.Epub;
saveOptions.encoding = "utf-8";

// By default, an output .epub document will have all its contents in one HTML part.
// A split criterion allows us to segment the document into several HTML parts.
// We will set the criteria to split the document into heading paragraphs.
// This is useful for readers who cannot read HTML files more significant than a specific size.
saveOptions.documentSplitCriteria = aw.Saving.DocumentSplitCriteria.HeadingParagraph;

// Specify that we want to export document properties.
saveOptions.exportDocumentProperties = true;

doc.save(base.artifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../)

