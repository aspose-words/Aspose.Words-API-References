---
title: XamlFlowSaveOptions.imagesFolder property
linktitle: imagesFolder property
articleTitle: imagesFolder property
second_title: Aspose.Words for NodeJs
description: "XamlFlowSaveOptions.imagesFolder property. Specifies the physical folder where images are saved when exporting a document to XAML format"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/xamlflowsaveoptions/imagesFolder/
---

## XamlFlowSaveOptions.imagesFolder property

Specifies the physical folder where images are saved when exporting a document to XAML format.
Default is an empty string.


```js
get imagesFolder(): string
```

### Remarks

When you save a [Document](../../../Aspose.Words/document/) in XAML format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [XamlFlowSaveOptions.imagesFolder](./) 
allows you to specify where the images will be saved and [XamlFlowSaveOptions.imagesFolderAlias](../imagesFolderAlias/) 
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the 
images in the same folder where the document file is saved. Use [XamlFlowSaveOptions.imagesFolder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, 
but still needs to save the images somewhere. In this case, you need to specify an accessible folder 
in the [XamlFlowSaveOptions.imagesFolder](./) property or provide custom streams via 
the [XamlFlowSaveOptions.imageSavingCallback](../imageSavingCallback/) event handler.




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
* property [XamlFlowSaveOptions.imagesFolderAlias](../imagesFolderAlias/)
* property [XamlFlowSaveOptions.imageSavingCallback](../imageSavingCallback/)

