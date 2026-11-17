---
title: Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName method
linktitle: get_UseSdtTagAsFormFieldName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName method. Specifies whether to use SDT control Tag or Id property as a name of form field in PDF in C++.'
type: docs
weight: 32500
url: /cpp/aspose.words.saving/pdfsaveoptions/get_usesdttagasformfieldname/
---
## PdfSaveOptions::get_UseSdtTagAsFormFieldName method


Specifies whether to use SDT control Tag or Id property as a name of form field in PDF.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName() const
```

## Remarks


The default value is **false**.

When set to **false**, SDT control Id property is used as a name of form field in PDF.

When set to **true**, SDT control Tag property is used as a name of form field in PDF.

If set to **true** and Tag is empty, Id property will be used as a form field name.

If set to **true** and Tag values are not unique, duplicate Tag values will be altered to build unique PDF form field names. 
## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
