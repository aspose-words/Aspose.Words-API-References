---
title: PdfSaveOptions.useSdtTagAsFormFieldName property
linktitle: useSdtTagAsFormFieldName property
articleTitle: useSdtTagAsFormFieldName property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.useSdtTagAsFormFieldName property. Specifies whether to use SDT control Tag or Id property as a name of form field in PDF."
type: docs
weight: 340
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/useSdtTagAsFormFieldName/
---

## PdfSaveOptions.useSdtTagAsFormFieldName property

Specifies whether to use SDT control Tag or Id property as a name of form field in PDF.


```js
get useSdtTagAsFormFieldName(): boolean
```

### Remarks

The default value is ``false``.

When set to ``false``, SDT control Id property is used as a name of form field in PDF.

When set to ``true``, SDT control Tag property is used as a name of form field in PDF.

If set to ``true`` and Tag is empty, Id property will be used as a form field name.

If set to ``true`` and Tag values are not unique, duplicate Tag values will be altered to build
unique PDF form field names.




### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

