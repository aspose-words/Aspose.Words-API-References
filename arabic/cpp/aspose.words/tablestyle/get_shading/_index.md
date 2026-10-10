---
title: "طريقة Aspose::Words::TableStyle::get_Shading"
linktitle: "get_Shading"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::TableStyle::get_Shading. يحصل على كائن Shading الذي يشير إلى تنسيق التظليل لخلايا الجدول في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words/tablestyle/get_shading/
---
## TableStyle::get_Shading method


يحصل على كائن [Shading](../../shading/) الذي يشير إلى تنسيق التظليل لخلايا الجدول.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::TableStyle::get_Shading()
```


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

* Class [Shading](../../shading/)
* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
