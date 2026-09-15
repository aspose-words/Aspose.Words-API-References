---
title: "طريقة Aspose::Words::TableStyle::get_LeftIndent"
linktitle: "get_LeftIndent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::TableStyle::get_LeftIndent. يحصل على أو يضبط القيمة التي تمثل الإزاحة اليسرى للجدول في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words/tablestyle/get_leftindent/
---
## TableStyle::get_LeftIndent method


يحصل أو يضبط القيمة التي تمثل المسافة البادئة اليسرى للجدول.

```cpp
double Aspose::Words::TableStyle::get_LeftIndent()
```


## أمثلة



يوضح كيفية تعيين موضع الجدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// فيما يلي طريقتان لمحاذاة جدول أفقيًا.
// 1 -  استخدم خاصية "Alignment" لمحاذاة الجدول إلى موقع على الصفحة، مثل الوسط:
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

// أدخل جدولًا وطبق النمط الذي أنشأناه عليه.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned to the center of the page");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

// 2 -  استخدم خاصية "LeftIndent" لتحديد مسافة إزاحة من الهامش الأيسر للصفحة:
tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle2"));
tableStyle->set_LeftIndent(55);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Green());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned according to left indent");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

doc->Save(get_ArtifactsDir() + u"Table.SetTableAlignment.docx");
```

## انظر أيضًا

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
