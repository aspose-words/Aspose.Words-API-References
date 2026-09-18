---
title: "Aspose::Words::Fields::FieldBarcode::get_FacingIdentificationMark Methode"
linktitle: "get_FacingIdentificationMark"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldBarcode::get_FacingIdentificationMark Methode. Liest oder setzt den Typ einer Facing Identification Mark (FIM), die in C++ eingefügt werden soll."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldbarcode/get_facingidentificationmark/
---
## FieldBarcode::get_FacingIdentificationMark method


Liest oder setzt den Typ eines Facing Identification Mark (FIM), das eingefügt werden soll.

```cpp
System::String Aspose::Words::Fields::FieldBarcode::get_FacingIdentificationMark()
```


## Beispiele



Zeigt, wie das BARCODE-Feld verwendet wird, um US-Postleitzahlen in Form eines Barcodes darzustellen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Im Folgenden werden zwei Methoden gezeigt, wie BARCODE-Felder verwendet werden, um benutzerdefinierte Werte als Barcodes darzustellen.
// 1 -  Speichern Sie den Wert, den der Barcode im Property PostalAddress anzeigen soll:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// Dieser Wert muss eine gültige Postleitzahl sein.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 -  Verweisen Sie auf ein Lesezeichen, das den Wert speichert, den dieser Barcode anzeigen soll:
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// Das Lesezeichen, auf das das BARCODE-Feld in seiner Property PostalAddress verweist
// muss ausschließlich die gültige Postleitzahl enthalten.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## Siehe auch

* Class [FieldBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
