---
title: MarkdownSaveOptions class
linktitle: MarkdownSaveOptions class
articleTitle: MarkdownSaveOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.MarkdownSaveOptions class. Class to specify additional options when saving a document into the [SaveFormat.Markdown](../../aspose.words/saveformat/#Markdown) format"
type: docs
weight: 450
url: /nodejs-net/aspose.words.saving/markdownsaveoptions/
---

## MarkdownSaveOptions class

Class to specify additional options when saving a document into the [SaveFormat.Markdown](../../aspose.words/saveformat/#Markdown) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [MarkdownSaveOptions](./) → [TxtSaveOptionsBase](../txtsaveoptionsbase/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [MarkdownSaveOptions()](./constructor/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Markdown](../../aspose.words/saveformat/#Markdown) format. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** .<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [emptyParagraphExportMode](./emptyParagraphExportMode/) | Specifies how to export empty paragraphs to Markdown. Default value is [MarkdownEmptyParagraphExportMode.EmptyLine](../markdownemptyparagraphexportmode/#EmptyLine). |
| [encoding](../txtsaveoptionsbase/encoding/) | Specifies the encoding to use when exporting in text formats.  Default value is .<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [exportAsHtml](./exportAsHtml/) | Allows to specify the elements to be exported to Markdown as raw HTML. Default value is [MarkdownExportAsHtml.None](../markdownexportashtml/#None). |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``true``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportHeadersFootersMode](../txtsaveoptionsbase/exportHeadersFootersMode/) | Specifies the way headers and footers are exported to the text formats. Default value is [TxtExportHeadersFootersMode.PrimaryOnly](../txtexportheadersfootersmode/#PrimaryOnly).<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [exportImagesAsBase64](./exportImagesAsBase64/) | Specifies whether images are saved in Base64 format to the output file. Default value is ``false``. |
| [exportUnderlineFormatting](./exportUnderlineFormatting/) | Gets or sets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". The default value is ``false``. |
| [forcePageBreaks](../txtsaveoptionsbase/forcePageBreaks/) | Allows to specify whether the page breaks should be preserved during export.<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [imageResolution](./imageResolution/) | Specifies the output resolution for images when exporting to Markdown. Default is ``96 dpi``. |
| [imageSavingCallback](./imageSavingCallback/) | Allows to control how images are saved when a document is saved to [SaveFormat.Markdown](../../aspose.words/saveformat/#Markdown) format. |
| [imagesFolder](./imagesFolder/) | Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.Markdown](../../aspose.words/saveformat/#Markdown) format. Default is an empty string. |
| [imagesFolderAlias](./imagesFolderAlias/) | Specifies the name of the folder used to construct image URIs written into a document. Default is an empty string. |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [linkExportMode](./linkExportMode/) | Specifies how links will be written to the output file. Default value is [MarkdownLinkExportMode.Auto](../markdownlinkexportmode/#Auto). |
| [listExportMode](./listExportMode/) | Specifies how list items will be written to the output file. Default value is [MarkdownListExportMode.MarkdownSyntax](../markdownlistexportmode/#MarkdownSyntax). |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [officeMathExportMode](./officeMathExportMode/) | Specifies how OfficeMath will be written to the output file. Default value is [MarkdownOfficeMathExportMode.Text](../markdownofficemathexportmode/#Text). |
| [paragraphBreak](../txtsaveoptionsbase/paragraphBreak/) | Specifies the string to use as a paragraph break when exporting in text formats.<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``true``, pretty formats output where applicable. Default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.Markdown](../../aspose.words/saveformat/#Markdown). |
| [tableContentAlignment](./tableContentAlignment/) | Gets or sets a value that specifies how to align contents in tables when exporting into the [SaveFormat.Markdown](../../aspose.words/saveformat/#Markdown) format. The default value is [TableContentAlignment.Auto](../tablecontentalignment/#Auto). |
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

Shows how to rename the image name during saving into Markdown document.

```js
test('RenameImages', () => {
  let doc = new aw.Document(base.myDir + "Rendering.docx");

  let saveOptions = new aw.Saving.MarkdownSaveOptions();
  // If we convert a document that contains images into Markdown, we will end up with one Markdown file which links to several images.
  // Each image will be in the form of a file in the local file system.
  // There is also a callback that can customize the name and file system location of each image.
  saveOptions.imageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
  saveOptions.saveFormat = aw.SaveFormat.Markdown;

  // The ImageSaving() method of our callback will be run at this time.
  doc.save(base.artifactsDir + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

  expect(Directory.GetFiles(base.artifactsDir) .Where(s => s.StartsWith(base.artifactsDir + "MarkdownSaveOptions.HandleDocument.md shape")) .Count(f => f.EndsWith(".jpeg"))).toEqual(1);
  expect(Directory.GetFiles(base.artifactsDir) .Where(s => s.StartsWith(base.artifactsDir + "MarkdownSaveOptions.HandleDocument.md shape")) .Count(f => f.EndsWith(".png"))).toEqual(8);
});


  /// <summary>
  /// Renames saved images that are produced when an Markdown document is saved.
  /// </summary>
public class SavedImageRename : IImageSavingCallback
{
  public SavedImageRename(string outFileName)
  {
    mOutFileName = outFileName;
  }

  void aw.Saving.IImageSavingCallback.imageSaving(ImageSavingArgs args)
  {
    string imageFileName = `${mOutFileName} shape ${++mCount}, of type ${args.currentShape.shapeType}${Path.GetExtension(args.imageFileName)}`;

    args.imageFileName = imageFileName;
    args.imageStream = new FileStream(base.artifactsDir + imageFileName, FileMode.create);

    expect(args.imageStream.CanWrite).toEqual(true);
    expect(args.isImageAvailable).toEqual(true);
    expect(args.keepImageStreamOpen).toEqual(false);
  }

  private int mCount;
  private readonly string mOutFileName;
}
```

### See Also

* module [Aspose.Words.Saving](../)
* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)

