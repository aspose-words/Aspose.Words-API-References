---
title: get_PreserveFormFields
second_title: Aspose.Words for C++ API Reference
description: Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is false.
type: docs
weight: 326
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

## Examples



Shows how to save a document to the PDF format using the Save method and the [PdfSaveOptions](../) class. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Insert a combo box which will allow a user to choose an option from a collection of strings.
builder->InsertComboBox(u"MyComboBox", MakeArray<String>({u"Apple", u"Banana", u"Cherry"}), 0);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto pdfOptions = MakeObject<PdfSaveOptions>();

// Set the "PreserveFormFields" property to "true" to save form fields as interactive objects in the output PDF.
// Set the "PreserveFormFields" property to "false" to freeze all form fields in the document at
// their current values and display them as plain text in the output PDF.
pdfOptions->set_PreserveFormFields(preserveFormFields);

doc->Save(ArtifactsDir + u"PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
