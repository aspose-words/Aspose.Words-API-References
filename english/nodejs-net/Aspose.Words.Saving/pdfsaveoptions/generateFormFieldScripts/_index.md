---
title: PdfSaveOptions.generateFormFieldScripts property
linktitle: generateFormFieldScripts property
articleTitle: generateFormFieldScripts property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.generateFormFieldScripts property. Specifies whether to generate scripts that emulate specific Microsoft Word form field behavior in PDF"
type: docs
weight: 190
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/generateFormFieldScripts/
---

## PdfSaveOptions.generateFormFieldScripts property

Specifies whether to generate scripts that emulate specific Microsoft Word form field behavior in PDF.
Default is ``false``.



```js
get generateFormFieldScripts(): boolean
```

### Remarks

When this option is enabled, the exporter generates PDF JavaScript actions to emulate Microsoft Word
form field behavior, such as date and time form fields with formatting and validation rules.

When set to ``true``, supported behavior will be exported as PDF JavaScript actions.
When set to ``false``, no form field scripts will be generated.

Script execution depends on the PDF viewer. Some PDF viewers might ignore scripts, restrict script execution,
or require the user to enable JavaScript.

JavaScript actions are prohibited by PDF/A-1, PDF/A-2 and PDF/A-3 compliance.
The ``false`` value will be used automatically in this case.




### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

