---
title: PdfSaveOptions.renderChoiceFormFieldBorder property
linktitle: renderChoiceFormFieldBorder property
articleTitle: renderChoiceFormFieldBorder property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.renderChoiceFormFieldBorder property. Specifies whether to render PDF choice form field border."
type: docs
weight: 290
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/renderChoiceFormFieldBorder/
---

## PdfSaveOptions.renderChoiceFormFieldBorder property

Specifies whether to render PDF choice form field border.


```js
get renderChoiceFormFieldBorder(): boolean
```

### Remarks

PDF choice form fields are used for export of SDT Combo Box Content Control, SDT Drop-Down List Content
Control and legacy Drop-Down Form Field when [PdfSaveOptions.preserveFormFields](../preserveFormFields/) option is enabled.

The default value is ``true``.




### Examples

Shows how to render PDF choice form field border.

```js
let doc = new aw.Document(base.myDir + "Legacy drop-down.docx");

let saveOptions = new aw.Saving.PdfSaveOptions();
saveOptions.preserveFormFields = true;
saveOptions.renderChoiceFormFieldBorder = true;

doc.save(base.artifactsDir + "PdfSaveOptions.renderChoiceFormFieldBorder.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

