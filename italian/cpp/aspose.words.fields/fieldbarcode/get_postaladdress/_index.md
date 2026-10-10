---
title: "Metodo Aspose::Words::Fields::FieldBarcode::get_PostalAddress"
linktitle: "get_PostalAddress"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldBarcode::get_PostalAddress. Ottiene o imposta l'indirizzo postale usato per generare un codice a barre o il nome del segnalibro che vi fa riferimento in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fields/fieldbarcode/get_postaladdress/
---
## FieldBarcode::get_PostalAddress method


Ottiene o imposta l'indirizzo postale utilizzato per generare un codice a barre o il nome del segnalibro che vi fa riferimento.

```cpp
System::String Aspose::Words::Fields::FieldBarcode::get_PostalAddress()
```


## Esempi



Mostra come utilizzare il campo BARCODE per visualizzare i codici ZIP statunitensi sotto forma di codice a barre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Di seguito sono riportati due modi per utilizzare i campi BARCODE per visualizzare valori personalizzati come codici a barre.
// 1 -  Memorizza il valore che il codice a barre visualizzerà nella proprietà PostalAddress:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// Questo valore deve essere un codice ZIP valido.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 -  Fai riferimento a un segnalibro che memorizza il valore che questo codice a barre visualizzerà:
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// Il segnalibro a cui il campo BARCODE fa riferimento nella sua proprietà PostalAddress
// deve contenere solo il codice ZIP valido.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## Vedi anche

* Class [FieldBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
