---
title: DocSaveOptions.alwaysCompressMetafiles property
linktitle: alwaysCompressMetafiles property
articleTitle: alwaysCompressMetafiles property
second_title: Aspose.Words for NodeJs
description: "DocSaveOptions.alwaysCompressMetafiles property. When ``False``, small metafiles are not compressed for performance reason"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Saving/docsaveoptions/alwaysCompressMetafiles/
---

## DocSaveOptions.alwaysCompressMetafiles property

When ``False``, small metafiles are not compressed for performance reason.
Default value is ``True``, all metafiles are compressed regardless of its size.



```js
get alwaysCompressMetafiles(): boolean
```

### Examples

Shows how to change metafiles compression in a document while saving.

```js
// Open a document that contains a Microsoft Equation 3.0 formula.
let doc = new aw.Document(base.myDir + "Microsoft equation object.docx");

// When we save a document, smaller metafiles are not compressed for performance reasons.
// We can set a flag in a SaveOptions object to compress every metafile when saving.
// Some editors such as LibreOffice cannot read uncompressed metafiles.
let saveOptions = new aw.Saving.DocSaveOptions();
saveOptions.alwaysCompressMetafiles = compressAllMetafiles;

doc.save(base.artifactsDir + "DocSaveOptions.alwaysCompressMetafiles.docx", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [DocSaveOptions](../)

