---
title: HtmlSaveOptions.cssStyleSheetFileName property
linktitle: cssStyleSheetFileName property
articleTitle: cssStyleSheetFileName property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.cssStyleSheetFileName property. Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML"
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/cssStyleSheetFileName/
---

## HtmlSaveOptions.cssStyleSheetFileName property

Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document
is exported to HTML.
Default is an empty string.


```js
get cssStyleSheetFileName(): string
```

### Remarks

This property has effect only when saving a document to HTML format
and external CSS style sheet is requested using [HtmlSaveOptions.cssStyleSheetType](../cssStyleSheetType/).

If this property is empty, the CSS file will be saved into the same folder and with the same name as the HTML
document but with the ".css" extension.

If only path but no file name is specified in this property, the CSS file will be saved into the specified
folder and will have the same name as the HTML document but with the ".css" extension.

If the folder specified by this property doesn't exist, it will be created automatically before the CSS file
is saved.

Another way to specify a folder where external CSS file is saved is to use [HtmlSaveOptions.resourceFolder](../resourceFolder/).





### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.resourceFolder](../resourceFolder/)
* property [HtmlSaveOptions.resourceFolderAlias](../resourceFolderAlias/)
* property [HtmlSaveOptions.cssStyleSheetType](../cssStyleSheetType/)

