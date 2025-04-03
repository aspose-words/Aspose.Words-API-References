---
title: SvgSaveOptions.resourcesFolderAlias property
linktitle: resourcesFolderAlias property
articleTitle: resourcesFolderAlias property
second_title: Aspose.Words for NodeJs
description: "SvgSaveOptions.resourcesFolderAlias property. Specifies the name of the folder used to construct image URIs written into an SVG document"
type: docs
weight: 90
url: /nodejs-net/Aspose.Words.Saving/svgsaveoptions/resourcesFolderAlias/
---

## SvgSaveOptions.resourcesFolderAlias property

Specifies the name of the folder used to construct image URIs written into an SVG document.
Default is ``None``.



```js
get resourcesFolderAlias(): string
```

### Remarks

When you save a [Document](../../../aspose.words/document/) in SVG format, Aspose.Words needs to save all
images embedded in the document as standalone files. [SvgSaveOptions.resourcesFolder](../resourcesFolder/)
allows you to specify where the images will be saved and [SvgSaveOptions.resourcesFolderAlias](./)
allows to specify how the image URIs will be constructed.




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
* property [SvgSaveOptions.resourcesFolder](../resourcesFolder/)

