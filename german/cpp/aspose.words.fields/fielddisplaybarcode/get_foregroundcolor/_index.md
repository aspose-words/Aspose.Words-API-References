---
title: "Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor Methode"
linktitle: "get_ForegroundColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor Methode. Liest oder setzt die Vordergrundfarbe des Barcode-Symbols. Gültige Werte liegen im Bereich [0, 0xFFFFFF] in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.fields/fielddisplaybarcode/get_foregroundcolor/
---
## FieldDisplayBarcode::get_ForegroundColor method


Liest oder setzt die Vordergrundfarbe des Barcode‑Symbols. Gültige Werte liegen im Bereich [0, 0xFFFFFF].

```cpp
System::String Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor()
```


## Beispiele



Zeigt, wie man ein DISPLAYBARCODE-Feld einfügt und seine Eigenschaften festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));

// Unten sind vier Arten von Barcodes aufgeführt, die auf verschiedene Weise dekoriert sind und die das DISPLAYBARCODE-Feld anzeigen kann.
// 1 -  QR-Code mit benutzerdefinierten Farben:
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

// 2 -  EAN13-Barcode, bei dem die Ziffern unter den Balken angezeigt werden:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  CODE39-Barcode:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  ITF4-Barcode, mit einem angegebenen Fallcode:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.DISPLAYBARCODE.docx");
```

## Siehe auch

* Class [FieldDisplayBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
