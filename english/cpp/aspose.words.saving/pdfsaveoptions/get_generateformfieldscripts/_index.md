---
title: Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts method
linktitle: get_GenerateFormFieldScripts
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts method. Specifies whether to generate scripts that emulate specific Microsoft Word form field behavior in PDF. Default is false in C++.'
type: docs
weight: 18500
url: /cpp/aspose.words.saving/pdfsaveoptions/get_generateformfieldscripts/
---
## PdfSaveOptions::get_GenerateFormFieldScripts method


Specifies whether to generate scripts that emulate specific Microsoft Word form field behavior in PDF. Default is **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts() const
```

## Remarks


When this option is enabled, the exporter generates PDF JavaScript actions to emulate Microsoft Word form field behavior, such as date and time form fields with formatting and validation rules.

When set to **true**, supported behavior will be exported as PDF JavaScript actions. When set to **false**, no form field scripts will be generated.

Script execution depends on the PDF viewer. Some PDF viewers might ignore scripts, restrict script execution, or require the user to enable JavaScript.

JavaScript actions are prohibited by PDF/A-1, PDF/A-2 and PDF/A-3 compliance. The **false** value will be used automatically in this case. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
