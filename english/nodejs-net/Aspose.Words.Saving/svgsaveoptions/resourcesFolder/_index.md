---
title: SvgSaveOptions.resourcesFolder property
linktitle: resourcesFolder property
articleTitle: resourcesFolder property
second_title: Aspose.Words for NodeJs
description: "SvgSaveOptions.resourcesFolder property. Specifies the physical folder where resources (images) are saved when exporting a document to Svg format"
type: docs
weight: 80
url: /nodejs-net/aspose.words.saving/svgsaveoptions/resourcesFolder/
---

## SvgSaveOptions.resourcesFolder property

Specifies the physical folder where resources (images) are saved when exporting a document to Svg format.
Default is ``null``.



```js
get resourcesFolder(): string
```

### Remarks

Has effect only if [SvgSaveOptions.exportEmbeddedImages](../exportEmbeddedImages/) property is ``false``.

When you save a [Document](../../../aspose.words/document/) in SVG format, Aspose.Words needs to save all
images embedded in the document as standalone files. [SvgSaveOptions.resourcesFolder](./)
allows you to specify where the images will be saved and [SvgSaveOptions.resourcesFolderAlias](../resourcesFolderAlias/)
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the
images in the same folder where the document file is saved. Use [SvgSaveOptions.resourcesFolder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images,
but still needs to save the images somewhere. In this case, you need to specify an accessible folder
in the [SvgSaveOptions.resourcesFolder](./) property




### Examples

Shows how to manipulate and print the URIs of linked resources created while converting a document to .svg.

```js
test.skip('SvgResourceFolder - TODO: sourceSavingCallback not supported yet', () => {
    let doc = new aw.Document(base.myDir + "Rendering.docx");

    let options = new aw.Saving.SvgSaveOptions();
    options.saveFormat = aw.SaveFormat.Svg;
    options.exportEmbeddedImages = false;
    options.resourcesFolder = base.artifactsDir + "SvgResourceFolder";
    options.resourcesFolderAlias = base.artifactsDir + "SvgResourceFolderAlias";
    options.showPageBorder = false;

    options.sourceSavingCallback = new ResourceUriPrinter()

    if (!fs.existsSync(options.resourcesFolderAlias)) {
      fs.mkdirSync(options.resourcesFolderAlias);
    }

    doc.save(base.artifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
  });

/*
  /// <summary>
  /// Counts and prints URIs of resources contained by as they are converted to .svg.
  /// </summary>
  private class ResourceUriPrinter : IResourceSavingCallback
  {
    void aw.Saving.IResourceSavingCallback.resourceSaving(ResourceSavingArgs args)
    {
      console.log(`Resource #${++mSavedResourceCount} \"${args.resourceFileName}\"`);
      console.log("\t" + args.resourceFileUri);
    }

    private int mSavedResourceCount;
  }
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SvgSaveOptions](../)
* property [SvgSaveOptions.resourcesFolderAlias](../resourcesFolderAlias/)

