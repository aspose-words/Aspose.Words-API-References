---
title: "Aspose::Words::Fields::FieldDisplayBarcode::get_CaseCodeStyle метод"
linktitle: "get_CaseCodeStyle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldDisplayBarcode::get_CaseCodeStyle метод. Получает или задает стиль кода упаковки (Case Code) для штрихкода типа ITF14. Допустимые значения — [STD|EXT|ADD] в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.fields/fielddisplaybarcode/get_casecodestyle/
---
## FieldDisplayBarcode::get_CaseCodeStyle method


Получает или задает стиль кода упаковки (Case Code) для штрихкода типа ITF14. Допустимые значения — [STD|EXT|ADD].

```cpp
System::String Aspose::Words::Fields::FieldDisplayBarcode::get_CaseCodeStyle()
```


## Примеры



Показывает, как вставить поле DISPLAYBARCODE и задать его свойства.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));

// Ниже представлены четыре типа штрихкодов, оформленных различными способами, которые может отображать поле DISPLAYBARCODE.
// 1 -  QR‑код с пользовательскими цветами:
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

// 2 -  Штрихкод EAN13, цифры отображаются под полосами:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  Штрихкод CODE39:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  штрих‑код ITF4 с указанным кодом корпуса:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.DISPLAYBARCODE.docx");
```

## См. также

* Class [FieldDisplayBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
