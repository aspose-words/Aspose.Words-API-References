---
title: Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields method
linktitle: get_PreserveFormFields
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields method. Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is false in C++.'
type: docs
weight: 28000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_preserveformfields/
---
## PdfSaveOptions::get_PreserveFormFields method


Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields() const
```

## Remarks


Microsoft Word form fields include text input, drop down and check box controls.

When set to **false**, these fields will be exported as text to PDF. When set to **true**, these fields will be exported as PDF form fields.

When exporting form fields to PDF as form fields, some formatting loss might occur because PDF form fields do not support all features of Microsoft Word form fields.

Also, the output size depends on the content size because editable forms in Microsoft Word are inline objects.

Editable forms are prohibited by PDF/A compliance. **false** value will be used automatically when saving to PDF/A.

Form fields are not supported when saving to PDF/UA. **false** value will be used automatically. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
