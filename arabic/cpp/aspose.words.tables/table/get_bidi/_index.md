---
title: "طريقة Aspose::Words::Tables::Table::get_Bidi"
linktitle: "get_Bidi"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Table::get_Bidi. يسترجع أو يضبط ما إذا كان هذا جدولًا من اليمين إلى اليسار في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.tables/table/get_bidi/
---
## Table::get_Bidi method


يحصل أو يضبط ما إذا كان هذا جدولًا من اليمين إلى اليسار.

```cpp
bool Aspose::Words::Tables::Table::get_Bidi()
```

## ملاحظات


عند **true**، تُرتّب الخلايا في هذا الصف من اليمين إلى اليسار.

القيمة الافتراضية هي **false**.

## أمثلة



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
