---
title: MarkdownSaveOptions.imageResolution property
linktitle: imageResolution property
articleTitle: imageResolution property
second_title: Aspose.Words for Node.js
description: "MarkdownSaveOptions.imageResolution property. Specifies the output resolution for images when exporting to Markdown"
type: docs
weight: 60
url: /nodejs-net/aspose.words.saving/markdownsaveoptions/imageResolution/
---

## MarkdownSaveOptions.imageResolution property

Specifies the output resolution for images when exporting to Markdown.
Default is ``96 dpi``.



```js
get imageResolution(): number
```

### Examples

Shows how to set the output resolution for images.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let saveOptions = new aw.Saving.MarkdownSaveOptions();
saveOptions.imageResolution = 300;

doc.save(base.artifactsDir + "MarkdownSaveOptions.imageResolution.md", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [MarkdownSaveOptions](../)

