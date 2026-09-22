---
title: "طريقة Aspose::Words::Tables::CellFormat::get_PreferredWidth"
linktitle: "get_PreferredWidth"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::CellFormat::get_PreferredWidth. تُرجع أو تُعيّن العرض المفضل للخلية في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.tables/cellformat/get_preferredwidth/
---
## CellFormat::get_PreferredWidth method


يرجع أو يضبط العرض المفضل للخلية.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::CellFormat::get_PreferredWidth()
```

## ملاحظات


العرض المفضل (بالإضافة إلى خيار الضبط التلقائي للجدول) يحدد كيفية حساب العرض الفعلي للخلية بواسطة خوارزمية تخطيط الجدول. يمكن تنفيذ تخطيط [Table](../../table/) بواسطة Aspose.Words عند حفظ المستند أو بواسطة Microsoft Word عند عرض المستند.

يمكن تحديد العرض المفضل بالنقاط أو بالنسبة المئوية. يمكن أيضاً تحديد العرض المفضل كـ "auto"، مما يعني عدم تحديد عرض مفضل.

القيمة الافتراضية هي [Auto](../../preferredwidth/auto/).

## أمثلة



يوضح كيفية تعيين عرض مفضل لخلايا الجدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// هناك طريقتان لتطبيق الفئة \"PreferredWidth\" على خلايا الجدول.
// 1 -  تعيين عرض مفضل ثابت بناءً على النقاط:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  تعيين عرض مفضل نسبي بناءً على نسبة من عرض الجدول:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// الخلية التي لا يُحدد لها عرض مفضل ستشغل باقي المساحة المتاحة.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// كل تكوين لخاصية \"PreferredWidth\" ينشئ كائنًا جديدًا.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## انظر أيضًا

* Class [PreferredWidth](../../preferredwidth/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
