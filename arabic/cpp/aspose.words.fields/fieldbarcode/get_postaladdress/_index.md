---
title: "Aspose::Words::Fields::FieldBarcode::get_PostalAddress طريقة"
linktitle: "get_PostalAddress"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldBarcode::get_PostalAddress طريقة. يحصل أو يضبط العنوان البريدي المستخدم لإنشاء الباركود أو اسم العلامة المرجعية التي تشير إليه في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.fields/fieldbarcode/get_postaladdress/
---
## FieldBarcode::get_PostalAddress method


يحصل أو يعيّن العنوان البريدي المستخدم لإنشاء رمز شريطي أو اسم الإشارة المرجعية التي تشير إليه.

```cpp
System::String Aspose::Words::Fields::FieldBarcode::get_PostalAddress()
```


## أمثلة



يظهر كيفية استخدام حقل BARCODE لعرض رموز ZIP الأمريكية على شكل رمز شريطي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// فيما يلي طريقتان لاستخدام حقول BARCODE لعرض قيم مخصصة كرموز شريطية.
// 1 - احفظ القيمة التي سيعرضها الباركود في الخاصية PostalAddress:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// يجب أن تكون هذه القيمة رمز ZIP صالح.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 - إشارة إلى إشارة مرجعية تخزن القيمة التي سيعرضها هذا الباركود:
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// الإشارة المرجعية التي يشير إليها حقل BARCODE في خاصية PostalAddress الخاصة به
// يجب أن تحتوي فقط على رمز ZIP صالح.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## انظر أيضًا

* Class [FieldBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
