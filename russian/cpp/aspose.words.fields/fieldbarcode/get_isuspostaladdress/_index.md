---
title: "метод Aspose::Words::Fields::FieldBarcode::get_IsUSPostalAddress"
linktitle: "get_IsUSPostalAddress"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Fields::FieldBarcode::get_IsUSPostalAddress. Получает или задает, является ли PostalAddress почтовым адресом США в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fields/fieldbarcode/get_isuspostaladdress/
---
## FieldBarcode::get_IsUSPostalAddress method


Получает или задает, является ли [PostalAddress](../get_postaladdress/) почтовым адресом США.

```cpp
bool Aspose::Words::Fields::FieldBarcode::get_IsUSPostalAddress()
```


## Примеры



Показывает, как использовать поле BARCODE для отображения почтовых индексов США в виде штрихкода.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Ниже представлены два способа использования полей BARCODE для отображения пользовательских значений в виде штрихкодов.
// 1 -  Сохраните значение, которое штрих-код будет отображать в свойстве PostalAddress:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// Это значение должно быть действительным почтовым индексом.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 -  Укажите закладку, которая хранит значение, отображаемое этим штрих-кодом:
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// Закладка, на которую ссылается поле BARCODE в своём свойстве PostalAddress
// должна содержать только действительный почтовый индекс.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## См. также

* Class [FieldBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
