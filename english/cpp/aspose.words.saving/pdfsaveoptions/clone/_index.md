---
title: Clone
second_title: Aspose.Words for C++ API Reference
description: Creates a deep clone of this object.
type: docs
weight: 27
url: /cpp/aspose.words.saving/pdfsaveoptions/clone/
---
## PdfSaveOptions::Clone method


Creates a deep clone of this object.

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfSaveOptions> Aspose::Words::Saving::PdfSaveOptions::Clone()
```


## Examples



Shows how to update all the fields in a document immediately before saving it to PDF. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert text with PAGE and NUMPAGES fields. These fields do not display the correct value in real time.
// We will need to manually update them using updating methods such as "Field.Update()", and "Document.UpdateFields()"
// each time we need them to display accurate values.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" of ");
builder->InsertField(u"NUMPAGES", u"");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Hello World!");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "UpdateFields" property to "false" to not update all the fields in a document right before a save operation.
// This is the preferable option if we know that all our fields will be up to date before saving.
// Set the "UpdateFields" property to "true" to iterate through all the document
// fields and update them before we save it as a PDF. This will make sure that all the fields will display
// the most accurate values in the PDF.
options->set_UpdateFields(updateFields);

// We can clone PdfSaveOptions objects.
ASPOSE_ASSERT_NS(options, options->Clone());

doc->Save(ArtifactsDir + u"PdfSaveOptions.UpdateFields.pdf", options);
```

## See Also

* Class [PdfSaveOptions](../)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
