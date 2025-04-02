---
title: MarkdownSaveOptions.imageSavingCallback property
linktitle: imageSavingCallback property
articleTitle: imageSavingCallback property
second_title: Aspose.Words for NodeJs
description: "MarkdownSaveOptions.imageSavingCallback property. Allows to control how images are saved when a document is saved to [SaveFormat.Markdown](../../../Aspose.Words/saveformat/#Markdown) format."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Saving/markdownsaveoptions/imageSavingCallback/
---

## MarkdownSaveOptions.imageSavingCallback property

Allows to control how images are saved when a document is saved to
[SaveFormat.Markdown](../../../Aspose.Words/saveformat/#Markdown) format.



```js
get imageSavingCallback(): Aspose.Words.Saving.IImageSavingCallback
```

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

* module [Aspose.Words.Saving](../../)
* class [MarkdownSaveOptions](../)

