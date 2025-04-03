---
title: ResourceSavingArgs.resourceFileName property
linktitle: resourceFileName property
articleTitle: resourceFileName property
second_title: Aspose.Words for NodeJs
description: "ResourceSavingArgs.resourceFileName property. Gets or sets the file name (without path) where the resource will be saved to."
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/resourcesavingargs/resourceFileName/
---

## ResourceSavingArgs.resourceFileName property

Gets or sets the file name (without path) where the resource will be saved to.


```js
get resourceFileName(): string
```

### Remarks

This property allows you to redefine how the resource file names are generated
during export to fixed page HTML or SVG.

When the event is fired, this property contains the file name that was generated 
by Aspose.Words. You can change the value of this property to save the resource into a 
different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every resource when 
exporting to fixed page HTML or SVG format. How the resource file name is generated 
depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated resource file name looks like 
*\<document base file name\>.\<image number\>.\<extension\>*.

When saving a document to a stream, the generated resource file name looks like 
*Aspose.Words.\<document guid\>.\<image number\>.\<extension\>*.

[ResourceSavingArgs.resourceFileName](./) must contain only the file name without the path.
Aspose.Words determines the path for saving and the value of the ``src`` attribute for writing 
to fixed page HTML or SVG using the document file name, the [HtmlFixedSaveOptions.resourcesFolder](../../htmlfixedsaveoptions/resourcesFolder/)
or [SvgSaveOptions.resourcesFolder](../../svgsaveoptions/resourcesFolder/) and [HtmlFixedSaveOptions.resourcesFolderAlias](../../htmlfixedsaveoptions/resourcesFolderAlias/) 
or [SvgSaveOptions.resourcesFolderAlias](../../svgsaveoptions/resourcesFolderAlias/) properties.

[HtmlFixedSaveOptions.resourcesFolder](../../htmlfixedsaveoptions/resourcesFolder/)
[SvgSaveOptions.resourcesFolder](../../svgsaveoptions/resourcesFolder/)
[HtmlFixedSaveOptions.resourcesFolderAlias](../../htmlfixedsaveoptions/resourcesFolderAlias/)
[SvgSaveOptions.resourcesFolderAlias](../../svgsaveoptions/resourcesFolderAlias/)



### See Also

* module [Aspose.Words.Saving](../../)
* class [ResourceSavingArgs](../)

