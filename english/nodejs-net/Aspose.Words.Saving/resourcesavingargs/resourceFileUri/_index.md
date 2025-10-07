---
title: ResourceSavingArgs.resourceFileUri property
linktitle: resourceFileUri property
articleTitle: resourceFileUri property
second_title: Aspose.Words for Node.js
description: "ResourceSavingArgs.resourceFileUri property. Gets or sets the uniform resource identifier (URI) used to reference the resource file from the document."
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/resourcesavingargs/resourceFileUri/
---

## ResourceSavingArgs.resourceFileUri property

Gets or sets the uniform resource identifier (URI) used to reference the resource file from the document.


```js
get resourceFileUri(): string
```

### Remarks

This property allows you to change URIs of resource files exported to fixed page HTML,
SVG or Markdown documents.

Aspose.Words automatically generates an URI for every resource file during export to fixed page HTML,
SVG or Markdown format. The generated URIs reference resource files saved by Aspose.Words. However, the URIs
can be incorrect if resource files are to be moved to other location or if resource files are saved to streams.
This property allows to correct URIs in these cases.

When the event is fired, this property contains the URI that was generated
by Aspose.Words. You can change the value of this property to provide a custom URI for the resource file.

[HtmlFixedSaveOptions.resourcesFolder](../../htmlfixedsaveoptions/resourcesFolder/)
[SvgSaveOptions.resourcesFolder](../../svgsaveoptions/resourcesFolder/)
[MarkdownSaveOptions.imagesFolder](../../markdownsaveoptions/imagesFolder/)
[HtmlFixedSaveOptions.resourcesFolderAlias](../../htmlfixedsaveoptions/resourcesFolderAlias/)
[SvgSaveOptions.resourcesFolderAlias](../../svgsaveoptions/resourcesFolderAlias/)
[MarkdownSaveOptions.imagesFolderAlias](../../markdownsaveoptions/imagesFolderAlias/)



### See Also

* module [Aspose.Words.Saving](../../)
* class [ResourceSavingArgs](../)

