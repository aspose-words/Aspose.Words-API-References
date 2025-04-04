---
title: XamlFixedSaveOptions.resourceSavingCallback property
linktitle: resourceSavingCallback property
articleTitle: resourceSavingCallback property
second_title: Aspose.Words for Node.js
description: "XamlFixedSaveOptions.resourceSavingCallback property. Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format."
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/xamlfixedsaveoptions/resourceSavingCallback/
---

## XamlFixedSaveOptions.resourceSavingCallback property

Allows to control how resources (images and fonts) are saved when a document is exported to fixed page Xaml format.


```js
get resourceSavingCallback(): Aspose.Words.Saving.IResourceSavingCallback
```

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

