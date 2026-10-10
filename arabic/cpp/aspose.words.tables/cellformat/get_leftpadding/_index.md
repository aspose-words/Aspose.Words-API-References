---
title: "Aspose::Words::Tables::CellFormat::get_LeftPadding طريقة"
linktitle: "get_LeftPadding"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::CellFormat::get_LeftPadding طريقة. تُرجع أو تُعيّن مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتويات الخلية في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.tables/cellformat/get_leftpadding/
---
## CellFormat::get_LeftPadding method


يرجع أو يضبط مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتويات الخلية.

```cpp
double Aspose::Words::Tables::CellFormat::get_LeftPadding()
```


## أمثلة



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
