---
title: "Aspose::Words::Tables::CellFormat::get_Width طريقة"
linktitle: "get_Width"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::CellFormat::get_Width طريقة. يحصل على عرض الخلية بالنقاط في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.tables/cellformat/get_width/
---
## CellFormat::get_Width method


يحصل على عرض الخلية بالنقاط.

```cpp
double Aspose::Words::Tables::CellFormat::get_Width()
```

## ملاحظات


يتم حساب العرض بواسطة Aspose.Words عند تحميل المستند وحفظه. حالياً، لا يتم دعم كل تركيبة من خصائص الجدول والخلية والمستند. قد لا تكون القيمة المرجعة دقيقة لبعض المستندات. قد لا يتطابق عرض الخلية تماماً مع ما يحسبه MS Word عند فتح المستند في MS Word.

لا يُنصح بتعيين هذه الخاصية. لا يوجد ضمان بأن الخلية ستحصل فعلياً على العرض المحدد. قد يتم تعديل العرض لاستيعاب محتويات الخلية في تخطيط جدول تلقائي الملاءمة. قد تكون خلايا الصفوف الأخرى لها إعدادات عرض متضاربة. قد يتم تغيير حجم الجدول ليتناسب مع الحاوية أو لتلبية إعدادات عرض الجدول. فكر في استخدام [PreferredWidth](../get_preferredwidth/) لتعيين عرض الخلية. تعيين هذه الخاصية يضبط [PreferredWidth](../get_preferredwidth/) ضمنياً منذ الإصدار 15.8.

## أمثلة



يوضح كيفية بناء جدول بحدود مخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// تعيين خيارات تنسيق الجدول لمنشئ المستند
// سيتم تطبيقها على كل صف وخلية نضيفها به.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// تغيير التنسيق سيطبقه على الخلية الحالية،
// وأي خلايا جديدة ننشئها باستخدام المنشئ لاحقًا.
// هذا لن يؤثر على الخلايا التي أضفناها مسبقًا.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// زد ارتفاع الصف لتناسب النص العمودي.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


يظهر كيفية تنسيق الخلايا باستخدام مُنشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// أدرج خلية ثانية، ثم قم بتكوين خيارات حشو نص الخلية.
// سيقوم المُنشئ بتطبيق هذه الإعدادات على خليةه الحالية، وأي خلايا جديدة تُنشأ لاحقًا.
builder->InsertCell();

System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = builder->get_CellFormat();
cellFormat->set_Width(250);
cellFormat->set_LeftPadding(30);
cellFormat->set_RightPadding(30);
cellFormat->set_TopPadding(30);
cellFormat->set_BottomPadding(30);

builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->EndTable();

// الخلية الأولى لم تتأثر بإعادة تكوين الحشو، ولا تزال تحتفظ بالقيم الافتراضية.
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_BottomPadding());

ASPOSE_ASSERT_EQ(250.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_BottomPadding());

// ستستمر الخلية الأولى في النمو في مستند الإخراج لتطابق حجم الخلية المجاورة لها.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetCellFormatting.docx");
```

## انظر أيضًا

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
