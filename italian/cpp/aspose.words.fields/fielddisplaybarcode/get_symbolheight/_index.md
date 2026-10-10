---
title: "Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolHeight metodo"
linktitle: "get_SymbolHeight"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolHeight metodo. Ottiene o imposta l'altezza del simbolo. L'unità è in TWIPS (1/1440 di pollice) in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.fields/fielddisplaybarcode/get_symbolheight/
---
## FieldDisplayBarcode::get_SymbolHeight method


Ottiene o imposta l'altezza del simbolo. L'unità è in TWIPS (1/1440 di pollice).

```cpp
System::String Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolHeight()
```


## Esempi



Mostra come inserire un campo DISPLAYBARCODE e impostarne le proprietà.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));

// Di seguito sono riportati quattro tipi di codici a barre, decorati in vari modi, che il campo DISPLAYBARCODE può visualizzare.
// 1 -  QR code con colori personalizzati:
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

// 2 -  Codice a barre EAN13, con le cifre visualizzate sotto le barre:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  Codice a barre CODE39:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  Codice a barre ITF4, con un codice di caso specificato:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.DISPLAYBARCODE.docx");
```

## Vedi anche

* Class [FieldDisplayBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
