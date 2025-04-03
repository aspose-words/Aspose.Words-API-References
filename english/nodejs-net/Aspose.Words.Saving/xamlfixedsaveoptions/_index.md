---
title: XamlFixedSaveOptions class
linktitle: XamlFixedSaveOptions class
articleTitle: XamlFixedSaveOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.XamlFixedSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.XamlFixed](../../aspose.words/saveformat/#XamlFixed) format"
type: docs
weight: 890
url: /nodejs-net/aspose.words.saving/xamlfixedsaveoptions/
---

## XamlFixedSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.XamlFixed](../../aspose.words/saveformat/#XamlFixed) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [XamlFixedSaveOptions](./) → [FixedPageSaveOptions](../fixedpagesaveoptions/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [XamlFixedSaveOptions()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [colorMode](../fixedpagesaveoptions/colorMode/) | Gets or sets a value determining how colors are rendered.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``true``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [jpegQuality](../fixedpagesaveoptions/jpegQuality/) | Gets or sets a value determining the quality of the JPEG images inside Html document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafileRenderingOptions](../fixedpagesaveoptions/metafileRenderingOptions/) | Allows to specify metafile rendering options.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [numeralFormat](../fixedpagesaveoptions/numeralFormat/) | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [optimizeOutput](../fixedpagesaveoptions/optimizeOutput/) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to ``true``.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [pageSavingCallback](../fixedpagesaveoptions/pageSavingCallback/) | Allows to control how separate pages are saved when a document is exported to fixed page format.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [pageSet](../fixedpagesaveoptions/pageSet/) | Gets or sets the pages to render. Default is all the pages in the document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``true``, pretty formats output where applicable. Default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [resourceSavingCallback](./resourceSavingCallback/) | Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format. |
| [resourcesFolder](./resourcesFolder/) | Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. Default is ``null``. |
| [resourcesFolderAlias](./resourcesFolderAlias/) | Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. Default is ``null``. |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.XamlFixed](../../aspose.words/saveformat/#XamlFixed). |
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

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```js
test('ResourceFolder', () => {
  let doc = new aw.Document(base.myDir + "Rendering.docx");
  let callback = new ResourceUriPrinter();

  // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
  // to modify how we save the document to the XAML save format.
  let options = new aw.Saving.XamlFixedSaveOptions();

  expect(options.saveFormat).toEqual(aw.SaveFormat.XamlFixed);

  // Use the "ResourcesFolder" property to assign a folder in the local file system into which
  // Aspose.words will save all the document's linked resources, such as images and fonts.
  options.resourcesFolder = base.artifactsDir + "XamlFixedResourceFolder";

  // Use the "ResourcesFolderAlias" property to use this folder
  // when constructing image URIs instead of the resources folder's name.
  options.resourcesFolderAlias = base.artifactsDir + "XamlFixedFolderAlias";

  options.resourceSavingCallback = callback;

  // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
  // We must ensure the folder exists before the callback's streams can put their resources into it.
  Directory.CreateDirectory(options.resourcesFolderAlias);

  doc.save(base.artifactsDir + "XamlFixedSaveOptions.resourceFolder.xaml", options);

  for (let resource of callback.Resources)
    console.log(resource);
});


  /// <summary>
  /// Counts and prints URIs of resources created during conversion to fixed .xaml.
  /// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
  public ResourceUriPrinter()
  {
    Resources = new aw.Lists.List<string>();
  }

  void aw.Saving.IResourceSavingCallback.resourceSaving(ResourceSavingArgs args)
  {
    Resources.add(`Resource \"${args.resourceFileName}\"\n\t${args.resourceFileUri}`);

      // If we specified a resource folder alias, we would also need
      // to redirect each stream to put its resource in the alias folder.
    args.resourceStream = new FileStream(args.resourceFileUri, FileMode.create);
    args.keepResourceStreamOpen = false;
  }

  public List<string> Resources { get; }
}
```

### See Also

* module [Aspose.Words.Saving](../)
* class [FixedPageSaveOptions](../fixedpagesaveoptions/)

