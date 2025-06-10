---
title: HtmlSaveOptions.cssStyleSheetType property
linktitle: cssStyleSheetType property
articleTitle: cssStyleSheetType property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.cssStyleSheetType property. Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB"
type: docs
weight: 60
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/cssStyleSheetType/
---

## HtmlSaveOptions.cssStyleSheetType property

Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB.
Default value is [CssStyleSheetType.Inline](../../cssstylesheettype/#Inline) for HTML/MHTML and
[CssStyleSheetType.External](../../cssstylesheettype/#External) for EPUB.



```js
get cssStyleSheetType(): Aspose.Words.Saving.CssStyleSheetType
```

### Remarks

Saving CSS style sheet into an external file is only supported when saving to HTML.
When you are exporting to one of the container formats (EPUB or MHTML) and specifying
[CssStyleSheetType.External](../../cssstylesheettype/#External), CSS file will be encapsulated
into the output package.




### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.cssStyleSheetFileName](../cssStyleSheetFileName/)

