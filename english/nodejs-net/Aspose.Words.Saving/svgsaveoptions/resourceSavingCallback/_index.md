---
title: SvgSaveOptions.resourceSavingCallback property
linktitle: resourceSavingCallback property
articleTitle: resourceSavingCallback property
second_title: Aspose.Words for NodeJs
description: "SvgSaveOptions.resourceSavingCallback property. Allows to control how resources (images) are saved when a document is exported to SVG format."
type: docs
weight: 70
url: /nodejs-net/aspose.words.saving/svgsaveoptions/resourceSavingCallback/
---

## SvgSaveOptions.resourceSavingCallback property

Allows to control how resources (images) are saved when a document is exported to SVG format.


```js
get resourceSavingCallback(): Aspose.Words.Saving.IResourceSavingCallback
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

