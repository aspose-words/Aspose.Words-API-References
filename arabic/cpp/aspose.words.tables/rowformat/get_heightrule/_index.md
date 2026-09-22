---
title: "طريقة Aspose::Words::Tables::RowFormat::get_HeightRule"
linktitle: "get_HeightRule"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::RowFormat::get_HeightRule. يحصل أو يضبط القاعدة لتحديد ارتفاع صف الجدول في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.tables/rowformat/get_heightrule/
---
## RowFormat::get_HeightRule method


يحصل أو يعيّن القاعدة لتحديد ارتفاع صف الجدول.

```cpp
Aspose::Words::HeightRule Aspose::Words::Tables::RowFormat::get_HeightRule()
```


## أمثلة



يظهر كيفية إنشاء جدول منسق باستخدام [DocumentBuilder](../../../aspose.words/documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
table->set_LeftIndent(20);

// قم بتعيين بعض خيارات التنسيق للنص ومظهر الجدول.
builder->get_RowFormat()->set_Height(40);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::AtLeast);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::FromArgb(198, 217, 241));

builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Bold(true);

// سيؤدي تكوين خيارات التنسيق في مُنشئ المستند إلى تطبيقها
// على الخلية/الصف الحالي الذي يوجد فيه المؤشر،
// وكذلك أي خلايا وصفوف جديدة تم إنشاؤها باستخدام ذلك المُنشئ.
builder->Write(u"Header Row,\n Cell 1");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 2");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 3");
builder->EndRow();

// أعد تكوين كائنات تنسيق المُنشئ للصفوف والخلايا الجديدة التي نحن على وشك إنشائها.
// لن يطبق المُنشئ هذه على الصف الأول الذي تم إنشاؤه بالفعل حتى يبرز كصف رأس.
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_White());
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_RowFormat()->set_Height(30);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
builder->InsertCell();
builder->get_Font()->set_Size(12);
builder->get_Font()->set_Bold(false);

builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 3.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 3.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateFormattedTable.docx");
```


يوضح كيفية تنسيق الصفوف باستخدام منشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// ابدأ صفًا ثانيًا، ثم قم بتكوين ارتفاعه. سيطبق المنشئ هذه الإعدادات على
// صفه الحالي، وكذلك أي صفوف جديدة ينشئها لاحقًا.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// لم يتأثر الصف الأول بإعادة تكوين الحشو ولا يزال يحتفظ بالقيم الافتراضية.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## انظر أيضًا

* Enum [HeightRule](../../../aspose.words/heightrule/)
* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
