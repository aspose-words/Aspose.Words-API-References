---
title: LoadOptions.mswVersion property
linktitle: mswVersion property
articleTitle: mswVersion property
second_title: Aspose.Words for NodeJs
description: "LoadOptions.mswVersion property. Allows to specify that the document loading process should match a specific MS Word version"
type: docs
weight: 100
url: /nodejs-net/Aspose.Words.Loading/loadoptions/mswVersion/
---

## LoadOptions.mswVersion property

Allows to specify that the document loading process should match a specific MS Word version.
Default value is [MsWordVersion.Word2019](../../../Aspose.Words.Settings/mswordversion/#Word2019)



```js
get mswVersion(): Aspose.Words.Settings.MsWordVersion
```

### Remarks

Different Word versions may handle certain aspects of document content and formatting slightly differently
during the loading process, which may result in minor differences in Document Object Model.


### Examples

Shows how to emulate the loading procedure of a specific Microsoft Word version during document loading.

```js
// By default, Aspose.words load documents according to Microsoft Word 2019 specification.
let loadOptions = new aw.Loading.LoadOptions();

expect(loadOptions.mswVersion).toEqual(aw.Settings.MsWordVersion.Word2019);

// This document is missing the default paragraph formatting style.
// This default style will be regenerated when we load the document either with Microsoft Word or Aspose.words.
loadOptions.mswVersion = aw.Settings.MsWordVersion.Word2007;
let doc = new aw.Document(base.myDir + "Document.docx", loadOptions);

// The style's line spacing will have this value when loaded by Microsoft Word 2007 specification.
expect(doc.styles.defaultParagraphFormat.lineSpacing).toBeCloseTo(12.95, 2);
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

