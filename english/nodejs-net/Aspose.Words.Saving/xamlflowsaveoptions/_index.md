---
title: XamlFlowSaveOptions class
linktitle: XamlFlowSaveOptions class
articleTitle: XamlFlowSaveOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.XamlFlowSaveOptions class. Can be used to specify additional options when saving a document into the  [SaveFormat.XamlFlow](../../Aspose.Words/saveformat/#XamlFlow) or [SaveFormat.XamlFlowPack](../../Aspose.Words/saveformat/#XamlFlowPack) format"
type: docs
weight: 900
url: /nodejs-net/Aspose.Words.Saving/xamlflowsaveoptions/
---

## XamlFlowSaveOptions class

Can be used to specify additional options when saving a document into the 
[SaveFormat.XamlFlow](../../Aspose.Words/saveformat/#XamlFlow) or [SaveFormat.XamlFlowPack](../../Aspose.Words/saveformat/#XamlFlowPack) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [XamlFlowSaveOptions](./) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [XamlFlowSaveOptions()](./XamlFlowSaveOptions/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XamlFlow](../../Aspose.Words/saveformat/#XamlFlow) format. |
| [XamlFlowSaveOptions(saveFormat)](./XamlFlowSaveOptions/#saveformat) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.XamlFlow](../../Aspose.Words/saveformat/#XamlFlow) or [SaveFormat.XamlFlowPack](../../Aspose.Words/saveformat/#XamlFlowPack) format. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [imageSavingCallback](./imageSavingCallback/) | Allows to control how images are saved when a document is saved to XAML. |
| [imagesFolder](./imagesFolder/) | Specifies the physical folder where images are saved when exporting a document to XAML format. Default is an empty string. |
| [imagesFolderAlias](./imagesFolderAlias/) | Specifies the name of the folder used to construct image URIs written into an XAML document. Default is an empty string. |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [replaceBackslashWithYenSign](./replaceBackslashWithYenSign/) | Specifies whether backslash characters should be replaced with yen signs. Default value is ``False``. |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XamlFlow](../../Aspose.Words/saveformat/#XamlFlow). |
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

Shows how to print the filenames of linked images created while converting a document to flow-form .xaml.

```js
test('ImageFolder', () => {
  let doc = new aw.Document(base.myDir + "Rendering.docx");

  let callback = new ImageUriPrinter(base.artifactsDir + "XamlFlowImageFolderAlias");

  // Create a "XamlFlowSaveOptions" object, which we can pass to the document's "Save" method
  // to modify how we save the document to the XAML save format.
  let options = new aw.Saving.XamlFlowSaveOptions();

  expect(options.saveFormat).toEqual(aw.SaveFormat.XamlFlow);

  // Use the "ImagesFolder" property to assign a folder in the local file system into which
  // Aspose.words will save all the document's linked images.
  options.imagesFolder = base.artifactsDir + "XamlFlowImageFolder";

  // Use the "ImagesFolderAlias" property to use this folder
  // when constructing image URIs instead of the images folder's name.
  options.imagesFolderAlias = base.artifactsDir + "XamlFlowImageFolderAlias";

  options.imageSavingCallback = callback;

  // A folder specified by "ImagesFolderAlias" will need to contain the resources instead of "ImagesFolder".
  // We must ensure the folder exists before the callback's streams can put their resources into it.
  Directory.CreateDirectory(options.imagesFolderAlias);

  doc.save(base.artifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

  for (let resource of callback.Resources)
    console.log(`${callback.imagesFolderAlias}/${resource}`);
});


  /// <summary>
  /// Counts and prints filenames of images while their parent document is converted to flow-form .xaml.
  /// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
  public ImageUriPrinter(string imagesFolderAlias)
  {
    ImagesFolderAlias = imagesFolderAlias;
    Resources = new aw.Lists.List<string>();
  }

  void aw.Saving.IImageSavingCallback.imageSaving(ImageSavingArgs args)
  {
    Resources.add(args.imageFileName);

      // If we specified an image folder alias, we would also need
      // to redirect each stream to put its image in the alias folder.
    args.imageStream = new FileStream(`${ImagesFolderAlias}/${args.imageFileName}`, FileMode.create);
    args.keepImageStreamOpen = false;
  }

  public string ImagesFolderAlias { get; }
  public List<string> Resources { get; }
}
```

### See Also

* module [Aspose.Words.Saving](../)
* class [SaveOptions](../saveoptions/)

