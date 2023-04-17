---
title: Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor method
linktitle: get_ForegroundColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor method. Gets or sets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF] in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.fields/fielddisplaybarcode/get_foregroundcolor/
---
## FieldDisplayBarcode::get_ForegroundColor method


Gets or sets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF].

```cpp
System::String Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor()
```


## Examples



Shows how to insert a DISPLAYBARCODE field, and set its properties. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto field = System::DynamicCast<FieldDisplayBarcode>(builder->InsertField(FieldType::FieldDisplayBarcode, true));

// Below are four types of barcodes, decorated in various ways, that the DISPLAYBARCODE field can display.
// 1 -  QR code with custom colors:
field->set_BarcodeType(u"QR");
field->set_BarcodeValue(u"ABC123");
field->set_BackgroundColor(u"0xF8BD69");
field->set_ForegroundColor(u"0xB5413B");
field->set_ErrorCorrectionLevel(u"3");
field->set_ScalingFactor(u"250");
field->set_SymbolHeight(u"1000");
field->set_SymbolRotation(u"0");

ASSERT_EQ(u" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field->GetFieldCode());
builder->Writeln();

// 2 -  EAN13 barcode, with the digits displayed below the bars:
field = System::DynamicCast<FieldDisplayBarcode>(builder->InsertField(FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  CODE39 barcode:
field = System::DynamicCast<FieldDisplayBarcode>(builder->InsertField(FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  ITF4 barcode, with a specified case code:
field = System::DynamicCast<FieldDisplayBarcode>(builder->InsertField(FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(ArtifactsDir + u"Field.DISPLAYBARCODE.docx");
```

## See Also

* Class [FieldDisplayBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
