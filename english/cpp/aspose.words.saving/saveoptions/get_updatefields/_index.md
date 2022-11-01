---
title: get_UpdateFields
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is true.
type: docs
weight: 183
url: /cpp/aspose.words.saving/saveoptions/get_updatefields/
---
## SaveOptions.get_UpdateFields method


Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateFields() const
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

