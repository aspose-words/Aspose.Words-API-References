---
title: XamlFlowSaveOptions.saveFormat property
linktitle: saveFormat property
articleTitle: saveFormat property
second_title: Aspose.Words for Node.js
description: "XamlFlowSaveOptions.saveFormat property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 60
url: /nodejs-net/aspose.words.saving/xamlflowsaveoptions/saveFormat/
---

## XamlFlowSaveOptions.saveFormat property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.XamlFlow](../../../aspose.words/saveformat/#XamlFlow).



```js
get saveFormat(): Aspose.Words.SaveFormat
```

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

* module [Aspose.Words.Saving](../../)
* class [XamlFlowSaveOptions](../)

