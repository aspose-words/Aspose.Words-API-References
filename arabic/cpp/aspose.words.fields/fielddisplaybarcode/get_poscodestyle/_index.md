---
title: "Aspose::Words::Fields::FieldDisplayBarcode::get_PosCodeStyle طريقة"
linktitle: "get_PosCodeStyle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldDisplayBarcode::get_PosCodeStyle طريقة. يحصل على أو يضبط نمط باركود نقطة البيع (أنواع الباركود UPCA|UPCE|EAN13|EAN8). القيم الصالحة (غير حساسة لحالة الأحرف) هي [STD|SUP2|SUP5|CASE] في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.fields/fielddisplaybarcode/get_poscodestyle/
---
## FieldDisplayBarcode::get_PosCodeStyle method


يحصل على أو يضبط نمط باركود نقطة البيع (أنواع الباركود UPCA|UPCE|EAN13|EAN8). القيم الصالحة (غير حساسة لحالة الأحرف) هي [STD|SUP2|SUP5|CASE].

```cpp
System::String Aspose::Words::Fields::FieldDisplayBarcode::get_PosCodeStyle()
```


## أمثلة



يعرض كيفية إدراج حقل DISPLAYBARCODE وتعيين خصائصه.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));

// فيما يلي أربعة أنواع من الباركود، مُزيّنة بطرق مختلفة، يمكن لحقل DISPLAYBARCODE عرضها.
// 1 -  رمز QR بألوان مخصصة:
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

// 2 -  باركود EAN13، مع الأرقام المعروضة أسفل الخطوط:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  باركود CODE39:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  باركود ITF4، مع رمز حالة محدد:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.DISPLAYBARCODE.docx");
```

## انظر أيضًا

* Class [FieldDisplayBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
