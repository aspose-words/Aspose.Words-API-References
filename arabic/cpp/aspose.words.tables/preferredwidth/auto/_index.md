---
title: "Aspose::Words::Tables::PreferredWidth::Auto طريقة"
linktitle: "تلقائي"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::PreferredWidth::Auto طريقة. تُرجع كائنًا يمثل القيمة \"العرض المفضل غير محدد\" في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.tables/preferredwidth/auto/
---
## PreferredWidth::Auto method


يرجع كائنًا يمثل القيمة \"العرض المفضل غير محدد\".

```cpp
static System::SharedPtr<Aspose::Words::Tables::PreferredWidth> & Aspose::Words::Tables::PreferredWidth::Auto()
```


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

* Class [PreferredWidth](../)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
