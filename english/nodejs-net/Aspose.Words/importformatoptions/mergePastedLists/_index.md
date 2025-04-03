---
title: ImportFormatOptions.mergePastedLists property
linktitle: mergePastedLists property
articleTitle: mergePastedLists property
second_title: Aspose.Words for NodeJs
description: "ImportFormatOptions.mergePastedLists property. Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists"
type: docs
weight: 70
url: /nodejs-net/aspose.words/importformatoptions/mergePastedLists/
---

## ImportFormatOptions.mergePastedLists property

Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists.
The default value is ``false``.



```js
get mergePastedLists(): boolean
```

### Examples

Shows how to merge lists from a documents.

```js
const srcDoc = new aw.Document(base.myDir + "List item.docx");
const dstDoc = new aw.Document(base.myDir + "List destination.docx");

const options = new aw.ImportFormatOptions();
options.mergePastedLists = true;

// Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
dstDoc.appendDocument(srcDoc, aw.ImportFormatMode.UseDestinationStyles, options);

dstDoc.save(base.artifactsDir + "Document.MergePastedLists.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ImportFormatOptions](../)

