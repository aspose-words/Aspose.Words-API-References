---
title: "Aspose::Words::TextOrientation enum"
linktitle: "TextOrientation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TextOrientation enum. يحدد اتجاه النص على صفحة، في خلية جدول أو إطار نص في C++."
type: docs
weight: 124000
url: /ar/cpp/aspose.words/textorientation/
---
## TextOrientation enum


يحدد اتجاه النص على الصفحة، في خلية جدول أو إطار نص.

```cpp
enum class TextOrientation
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| أفقي | 0 | النص مُرتب أفقيًا (lr-tb). |
| أسفل | 1 | النص مُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl). |
| أعلى | 3 | النص مُدوَّر 90 درجة إلى اليسار ليظهر من الأسفل إلى الأعلى (bt-lr). |
| HorizontalRotatedFarEast | 4 | النص مُرتب أفقيًا، لكن أحرف الشرق الأقصى مُدوَّرة 90 درجة إلى اليسار (lr-tb-v). |
| VerticalFarEast | 5 | تظهر أحرف الشرق الأقصى عموديًا، والنص الآخر يُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل (tb-rl-v). |
| VerticalRotatedFarEast | 7 | تظهر أحرف الشرق الأقصى عموديًا، والنص الآخر يُدوَّر 90 درجة إلى اليمين ليظهر من الأعلى إلى الأسفل عموديًا، ثم من اليسار إلى اليمين أفقيًا (tb-lr-v). |


## أمثلة



يظهر كيفية إنشاء جدول منسق 2×2.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// أثناء بناء الجدول، سيطبق مُنشئ المستند قيم خصائص RowFormat/CellFormat الحالية.
// على الصف/الخلية الحالية التي يقع فيها المؤشر وأي صفوف/خلايا جديدة يتم إنشاؤها.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// الصفوف والخلايا التي أضيفت مسبقًا لا تتأثر بأية تغييرات لاحقة على تنسيق المُنشئ.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
