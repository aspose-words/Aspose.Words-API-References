---
title: get_IsUSPostalAddress
second_title: Aspose.Words for C++ API Reference
description: Gets or sets whether PostalAddress is a U.S. postal address.
type: docs
weight: 40
url: /cpp/aspose.words.fields/fieldbarcode/get_isuspostaladdress/
---
## FieldBarcode::get_IsUSPostalAddress method


Gets or sets whether [PostalAddress](../get_postaladdress/) is a U.S. postal address.

```cpp
bool Aspose::Words::Fields::FieldBarcode::get_IsUSPostalAddress()
```


## Examples



Shows how to use the BARCODE field to display U.S. ZIP codes in the form of a barcode. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln();

// Below are two ways of using BARCODE fields to display custom values as barcodes.
// 1 -  Store the value that the barcode will display in the PostalAddress property:
auto field = System::DynamicCast<FieldBarcode>(builder->InsertField(FieldType::FieldBarcode, true));

// This value needs to be a valid ZIP code.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(BreakType::LineBreak);

// 2 -  Reference a bookmark that stores the value that this barcode will display:
field = System::DynamicCast<FieldBarcode>(builder->InsertField(FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// The bookmark that the BARCODE field references in its PostalAddress property
// need to contain nothing besides the valid ZIP code.
builder->InsertBreak(BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(ArtifactsDir + u"Field.BARCODE.docx");
```

## See Also

* Class [FieldBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
