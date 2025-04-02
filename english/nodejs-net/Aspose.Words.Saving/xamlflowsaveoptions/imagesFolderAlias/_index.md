---
title: XamlFlowSaveOptions.imagesFolderAlias property
linktitle: imagesFolderAlias property
articleTitle: imagesFolderAlias property
second_title: Aspose.Words for NodeJs
description: "XamlFlowSaveOptions.imagesFolderAlias property. Specifies the name of the folder used to construct image URIs written into an XAML document"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Saving/xamlflowsaveoptions/imagesFolderAlias/
---

## XamlFlowSaveOptions.imagesFolderAlias property

Specifies the name of the folder used to construct image URIs written into an XAML document.
Default is an empty string.


```js
get imagesFolderAlias(): string
```

### Remarks

When you save a [Document](../../../Aspose.Words/document/) in XAML format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [XamlFlowSaveOptions.imagesFolder](../imagesFolder/) 
allows you to specify where the images will be saved and [XamlFlowSaveOptions.imagesFolderAlias](./) 
allows to specify how the image URIs will be constructed.

If [XamlFlowSaveOptions.imagesFolderAlias](./) is not an empty string, then the image URI written
to XAML will be *ImagesFolderAlias + \<image file name\>*.

If [XamlFlowSaveOptions.imagesFolderAlias](./) is an empty string, then the image URI written 
to XAML will be *ImagesFolder + \<image file name\>*.

If [XamlFlowSaveOptions.imagesFolderAlias](./) is set to '.' (dot), then the image file name 
will be written to XAML without path regardless of other options.




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
* property [XamlFlowSaveOptions.imagesFolder](../imagesFolder/)
* property [XamlFlowSaveOptions.imageSavingCallback](../imageSavingCallback/)

