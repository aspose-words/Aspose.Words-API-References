---
title: "Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeValue méthode"
linktitle: "get_BarcodeValue"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeValue méthode. Obtient ou définit la valeur du code‑barres en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fields/fielddisplaybarcode/get_barcodevalue/
---
## FieldDisplayBarcode::get_BarcodeValue method


Obtient ou définit la valeur du code-barres.

```cpp
System::String Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeValue()
```


## Exemples



Montre comment insérer un champ DISPLAYBARCODE et définir ses propriétés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));

// Ci-dessous quatre types de codes-barres, décorés de différentes manières, que le champ DISPLAYBARCODE peut afficher.
// 1 -  QR code avec des couleurs personnalisées :
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

// 2 -  code-barres EAN13, avec les chiffres affichés sous les barres :
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  code-barres CODE39 :
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  code-barres ITF4, avec un code de cas spécifié:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.DISPLAYBARCODE.docx");
```

## Voir aussi

* Class [FieldDisplayBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
