---
title: "Aspose::Words::Fields::FieldBarcode::get_IsBookmark yöntemi"
linktitle: "get_IsBookmark"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldBarcode::get_IsBookmark yöntemi. C++'ta PostalAddress'in bir yer imi adı olup olmadığını alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fields/fieldbarcode/get_isbookmark/
---
## FieldBarcode::get_IsBookmark method


[PostalAddress](../get_postaladdress/) 'in bir yer imi adı olup olmadığını alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldBarcode::get_IsBookmark()
```


## Örnekler



BARCODE alanını kullanarak ABD ZIP kodlarını barkod biçiminde nasıl görüntüleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Aşağıda, BARCODE alanlarını kullanarak özel değerleri barkod olarak görüntülemenin iki yolu verilmiştir.
// 1 -  Barkodun PostalAddress özelliğinde göstereceği değeri depolayın:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// Bu değer geçerli bir posta kodu olmalıdır.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 -  Bu barkodun göstereceği değeri depolayan bir yer imine referans ver:
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// BARCODE alanının PostalAddress özelliğinde referans verdiği yer imi
// geçerli posta kodu dışında hiçbir şey içermemelidir.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## Ayrıca Bakınız

* Class [FieldBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
