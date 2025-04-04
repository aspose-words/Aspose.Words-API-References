---
title: SvgSaveOptions.exportEmbeddedImages property
linktitle: exportEmbeddedImages property
articleTitle: exportEmbeddedImages property
second_title: Aspose.Words for Node.js
description: "SvgSaveOptions.exportEmbeddedImages property. Specifies whether images should be embedded into the SVG document as base64"
type: docs
weight: 20
url: /nodejs-net/aspose.words.saving/svgsaveoptions/exportEmbeddedImages/
---

## SvgSaveOptions.exportEmbeddedImages property

Specifies whether images should be embedded into the SVG document as base64.
Be aware that activating this option can lead to a significant increase in the size of the output SVG file.


```js
get exportEmbeddedImages(): boolean
```

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

