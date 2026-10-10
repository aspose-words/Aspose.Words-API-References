---
title: "Aspose::Words::Tables::Table::get_CellSpacing طريقة"
linktitle: "get_CellSpacing"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::get_CellSpacing طريقة. يحصل أو يضبط مقدار المسافة (بوحدات النقاط) بين الخلايا في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words.tables/table/get_cellspacing/
---
## Table::get_CellSpacing method


يحصل أو يضبط مقدار المسافة (بالنقاط) بين الخلايا.

```cpp
double Aspose::Words::Tables::Table::get_CellSpacing()
```


## أمثلة



يظهر كيفية تمكين التباعد بين الخلايا الفردية في جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Animal");
builder->InsertCell();
builder->Write(u"Class");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Dog");
builder->InsertCell();
builder->Write(u"Mammal");
builder->EndTable();

table->set_CellSpacing(3);

// عيّن الخاصية "AllowCellSpacing" إلى "true" لتمكين التباعد بين الخلايا
// بقيمة مساوية لقيمة الخاصية "CellSpacing"، بالنقاط.
// عيّن الخاصية "AllowCellSpacing" إلى "false" لتعطيل التباعد بين الخلايا
// وتجاهل قيمة الخاصية "CellSpacing".
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// تعديل الخاصية "CellSpacing" سيفعل تلقائيًا التباعد بين الخلايا.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```


يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// قد يؤدي ضبط خصائص النمط للجدول إلى تأثير على خصائص الجدول نفسه.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## انظر أيضًا

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
