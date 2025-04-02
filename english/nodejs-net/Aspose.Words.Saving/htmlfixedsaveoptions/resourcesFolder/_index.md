---
title: HtmlFixedSaveOptions.resourcesFolder property
linktitle: resourcesFolder property
articleTitle: resourcesFolder property
second_title: Aspose.Words for NodeJs
description: "HtmlFixedSaveOptions.resourcesFolder property. Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format"
type: docs
weight: 160
url: /nodejs-net/Aspose.Words.Saving/htmlfixedsaveoptions/resourcesFolder/
---

## HtmlFixedSaveOptions.resourcesFolder property

Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format.
Default is ``None``.



```js
get resourcesFolder(): string
```

### Remarks

Has effect only if [HtmlFixedSaveOptions.exportEmbeddedImages](../exportEmbeddedImages/) property is ``False``.

When you save a [Document](../../../Aspose.Words/document/) in Html format, Aspose.Words needs to save all
images embedded in the document as standalone files. [HtmlFixedSaveOptions.resourcesFolder](./)
allows you to specify where the images will be saved and [HtmlFixedSaveOptions.resourcesFolderAlias](../resourcesFolderAlias/)
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the
images in the same folder where the document file is saved. Use [HtmlFixedSaveOptions.resourcesFolder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images,
but still needs to save the images somewhere. In this case, you need to specify an accessible folder
by using the [HtmlFixedSaveOptions.resourcesFolder](./) property




### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)
* property [HtmlFixedSaveOptions.resourcesFolderAlias](../resourcesFolderAlias/)

