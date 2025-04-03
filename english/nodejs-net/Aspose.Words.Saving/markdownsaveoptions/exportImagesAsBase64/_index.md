---
title: MarkdownSaveOptions.exportImagesAsBase64 property
linktitle: exportImagesAsBase64 property
articleTitle: exportImagesAsBase64 property
second_title: Aspose.Words for NodeJs
description: "MarkdownSaveOptions.exportImagesAsBase64 property. Specifies whether images are saved in Base64 format to the output file"
type: docs
weight: 30
url: /nodejs-net/aspose.words.saving/markdownsaveoptions/exportImagesAsBase64/
---

## MarkdownSaveOptions.exportImagesAsBase64 property

Specifies whether images are saved in Base64 format to the output file.
Default value is ``false``.



```js
get exportImagesAsBase64(): boolean
```

### Remarks

When this property is set to ``true`` images data are exported
directly into the **img** elements and separate files are not created.




### Examples

Shows how to save a .md document with images embedded inside it.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

let saveOptions = new aw.Saving.MarkdownSaveOptions { ExportImagesAsBase64 = exportImagesAsBase64 };

doc.save(base.artifactsDir + "MarkdownSaveOptions.exportImagesAsBase64.md", saveOptions);

let outDocContents = fs.readFileSync(base.artifactsDir + "MarkdownSaveOptions.exportImagesAsBase64.md").toString();

Assert.true(exportImagesAsBase64
  ? outDocContents.contains("data:image/jpeg;base64")
  : outDocContents.contains("MarkdownSaveOptions.exportImagesAsBase64.001.jpeg"));
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [MarkdownSaveOptions](../)

