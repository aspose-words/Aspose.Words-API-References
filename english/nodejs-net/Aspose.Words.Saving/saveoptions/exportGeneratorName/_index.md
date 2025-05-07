---
title: SaveOptions.exportGeneratorName property
linktitle: exportGeneratorName property
articleTitle: exportGeneratorName property
second_title: Aspose.Words for Node.js
description: "SaveOptions.exportGeneratorName property. When ``true``, causes the name and version of Aspose.Words to be embedded into produced files"
type: docs
weight: 60
url: /nodejs-net/aspose.words.saving/saveoptions/exportGeneratorName/
---

## SaveOptions.exportGeneratorName property

When ``true``, causes the name and version of Aspose.Words to be embedded into produced files.
Default value is ``true``.



```js
get exportGeneratorName(): boolean
```

### Examples

Shows how to disable adding name and version of Aspose.words into produced files.

```js
let doc = new aw.Document();

// Use https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ to know how to check the result.
let saveOptions = new aw.Saving.OoxmlSaveOptions();
saveOptions.exportGeneratorName = false;

doc.save(base.artifactsDir + "OoxmlSaveOptions.exportGeneratorName.docx", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SaveOptions](../)

