---
title: "Aspose::Words::Tables::PreferredWidth::Equals طريقة"
linktitle: "Equals"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::PreferredWidth::Equals طريقة. يحدد ما إذا كان PreferredWidth المحدد يساوي في القيمة PreferredWidth الحالي في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.tables/preferredwidth/equals/
---
## PreferredWidth::Equals(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) method


يحدد ما إذا كان [PreferredWidth](../) المحدد يساوي في القيمة [PreferredWidth](../) الحالي.

```cpp
bool Aspose::Words::Tables::PreferredWidth::Equals(const System::SharedPtr<Aspose::Words::Tables::PreferredWidth> &other)
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
## PreferredWidth::Equals(System::SharedPtr\<System::Object\>) method


يحدد ما إذا كان الكائن المحدد مساوٍ في القيمة للكائن الحالي.

```cpp
bool Aspose::Words::Tables::PreferredWidth::Equals(System::SharedPtr<System::Object> obj) override
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
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
