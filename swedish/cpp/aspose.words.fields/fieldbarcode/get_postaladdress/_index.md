---
title: "Aspose::Words::Fields::FieldBarcode::get_PostalAddress metod"
linktitle: "get_PostalAddress"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldBarcode::get_PostalAddress metod. Hämtar eller anger den postadress som används för att generera en streckkod eller namnet på bokmärket som refererar till den i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.fields/fieldbarcode/get_postaladdress/
---
## FieldBarcode::get_PostalAddress method


Hämtar eller anger postadressen som används för att generera en streckkod eller namnet på bokmärket som refererar till den.

```cpp
System::String Aspose::Words::Fields::FieldBarcode::get_PostalAddress()
```


## Exempel



Visar hur man använder BARCODE-fältet för att visa amerikanska postnummer i form av en streckkod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Nedan finns två sätt att använda BARCODE-fält för att visa anpassade värden som streckkoder.
// 1 -  Spara värdet som streckkoden ska visa i egenskapen PostalAddress:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// Detta värde måste vara ett giltigt postnummer.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 -  Referera till ett bokmärke som lagrar värdet som denna streckkod ska visa:
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// Bokmärket som BARCODE-fältet refererar till i sin egenskap PostalAddress
// måste bara innehålla det giltiga postnumret.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## Se även

* Class [FieldBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
