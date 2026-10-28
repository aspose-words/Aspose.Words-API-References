---
title: Aspose::Words::Fields::FieldBarcode::set_FacingIdentificationMark method
linktitle: set_FacingIdentificationMark
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldBarcode::set_FacingIdentificationMark method. Sets the type of a Facing Identification Mark (FIM) to insert in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.fields/fieldbarcode/set_facingidentificationmark/
---
## FieldBarcode::set_FacingIdentificationMark method


Sets the type of a Facing Identification Mark (FIM) to insert.

```cpp
void Aspose::Words::Fields::FieldBarcode::set_FacingIdentificationMark(const System::String & value)
```

## Examples


Shows how to use the BARCODE field to display U.S. ZIP codes in the form of a barcode.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Below are two ways of using BARCODE fields to display custom values as barcodes.
// 1 -  Store the value that the barcode will display in the PostalAddress property:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(FieldType::FieldBarcode, true));

// This value needs to be a valid ZIP code.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(BreakType::LineBreak);

// 2 -  Reference a bookmark that stores the value that this barcode will display:
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// The bookmark that the BARCODE field references in its PostalAddress property
// need to contain nothing besides the valid ZIP code.
builder->InsertBreak(BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```
## See Also

* Class [FieldBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
