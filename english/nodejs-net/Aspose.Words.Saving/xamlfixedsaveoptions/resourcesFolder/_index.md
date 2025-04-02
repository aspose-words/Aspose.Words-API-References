---
title: XamlFixedSaveOptions.resourcesFolder property
linktitle: resourcesFolder property
articleTitle: resourcesFolder property
second_title: Aspose.Words for NodeJs
description: "XamlFixedSaveOptions.resourcesFolder property. Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/xamlfixedsaveoptions/resourcesFolder/
---

## XamlFixedSaveOptions.resourcesFolder property

Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format.
Default is ``None``.



```js
get resourcesFolder(): string
```

### Remarks

When you save a [Document](../../../Aspose.Words/document/) in fixed page Xaml format, Aspose.Words needs to save all
images embedded in the document as standalone files. [XamlFixedSaveOptions.resourcesFolder](./)
allows you to specify where the images will be saved and [XamlFixedSaveOptions.resourcesFolderAlias](../resourcesFolderAlias/)
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the
images in the same folder where the document file is saved. Use [XamlFixedSaveOptions.resourcesFolder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images,
but still needs to save the images somewhere. In this case, you need to specify an accessible folder
by using the [XamlFixedSaveOptions.resourcesFolder](./) property




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

* module [Aspose.Words.Saving](../../)
* class [XamlFixedSaveOptions](../)
* property [XamlFixedSaveOptions.resourcesFolderAlias](../resourcesFolderAlias/)

