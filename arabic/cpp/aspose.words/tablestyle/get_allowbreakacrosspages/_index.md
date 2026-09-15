---
title: "طريقة Aspose::Words::TableStyle::get_AllowBreakAcrossPages"
linktitle: "get_AllowBreakAcrossPages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::TableStyle::get_AllowBreakAcrossPages. يحصل أو يعيّن علامة تشير إلى ما إذا كان مسموحًا للنص في صف جدول أن ينقسم عبر فاصل صفحة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/tablestyle/get_allowbreakacrosspages/
---
## TableStyle::get_AllowBreakAcrossPages method


يحصل أو يضبط علامة تشير إلى ما إذا كان مسموحًا للنص في صف الجدول أن ينقسم عبر فاصل صفحة.

```cpp
bool Aspose::Words::TableStyle::get_AllowBreakAcrossPages()
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

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
