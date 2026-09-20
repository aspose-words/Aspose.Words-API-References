---
title: "Aspose::Words::Fields::FieldBarcode::get_PostalAddress método"
linktitle: "get_PostalAddress"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldBarcode::get_PostalAddress método. Obtiene o establece la dirección postal utilizada para generar un código de barras o el nombre del marcador que lo refiere en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.fields/fieldbarcode/get_postaladdress/
---
## FieldBarcode::get_PostalAddress method


Obtiene o establece la dirección postal utilizada para generar un código de barras o el nombre del marcador que la referencia.

```cpp
System::String Aspose::Words::Fields::FieldBarcode::get_PostalAddress()
```


## Ejemplos



Muestra cómo usar el campo BARCODE para mostrar códigos ZIP de EE. UU. en forma de código de barras.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// A continuación se presentan dos formas de usar campos BARCODE para mostrar valores personalizados como códigos de barras.
// 1 -  Almacene el valor que el código de barras mostrará en la propiedad PostalAddress:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// Este valor debe ser un código postal válido.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 -  Referencie un marcador que almacene el valor que este código de barras mostrará:
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// El marcador que el campo BARCODE referencia en su propiedad PostalAddress
// debe contener únicamente el código postal válido.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## Ver también

* Class [FieldBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
