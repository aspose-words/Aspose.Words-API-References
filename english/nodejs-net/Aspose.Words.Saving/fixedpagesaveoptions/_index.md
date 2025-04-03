---
title: FixedPageSaveOptions class
linktitle: FixedPageSaveOptions class
articleTitle: FixedPageSaveOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.FixedPageSaveOptions class. Contains common options that can be specified when saving a document into fixed page formats (PDF, XPS, images etc)"
type: docs
weight: 190
url: /nodejs-net/aspose.words.saving/fixedpagesaveoptions/
---

## FixedPageSaveOptions class

Contains common options that can be specified when saving a document into fixed page formats (PDF, XPS,
images etc).
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [FixedPageSaveOptions](./) → [SaveOptions](../saveoptions/)

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [colorMode](./colorMode/) | Gets or sets a value determining how colors are rendered. |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``true``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [jpegQuality](./jpegQuality/) | Gets or sets a value determining the quality of the JPEG images inside Html document. |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafileRenderingOptions](./metafileRenderingOptions/) | Allows to specify metafile rendering options. |
| [numeralFormat](./numeralFormat/) | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default. |
| [optimizeOutput](./optimizeOutput/) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to ``true``. |
| [pageSavingCallback](./pageSavingCallback/) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [pageSet](./pageSet/) | Gets or sets the pages to render. Default is all the pages in the document. |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``true``, pretty formats output where applicable. Default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [saveFormat](../saveoptions/saveFormat/) | Specifies the format in which the document will be saved if this save options object is used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
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

Shows how to render one page from a document to a JPEG image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 2.");
builder.insertImage(base.imageDir + "Logo.jpg");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let options = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Jpeg);
// Set the "PageSet" to "1" to select the second page via
// the zero-based index to start rendering the document from.
options.pageSet = new aw.Saving.PageSet(1);

// When we save the document to the JPEG format, Aspose.words only renders one page.
// This image will contain one page starting from page two,
// which will just be the second page of the original document.
doc.save(base.artifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

Shows how to render every page of a document to a separate TIFF image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 2.");
builder.insertImage(base.imageDir + "Logo.jpg");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let options = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Tiff);

for (let i = 0; i < doc.pageCount; i++)
{
  // Set the "PageSet" property to the number of the first page from
  // which to start rendering the document from.
  options.pageSet = new aw.Saving.PageSet(i);
  // Export page at 2325x5325 pixels and 600 dpi.
  options.resolution = 600;
  options.imageSize2 = new aw.JSSize(2325, 5325);

  doc.save(base.artifactsDir + `ImageSaveOptions.PageByPage.${i + 1}.tiff`, options);
}
```

### See Also

* module [Aspose.Words.Saving](../)
* class [SaveOptions](../saveoptions/)

