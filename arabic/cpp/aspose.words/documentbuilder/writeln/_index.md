---
title: "Aspose::Words::DocumentBuilder::Writeln طريقة"
linktitle: "Writeln"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::Writeln طريقة. يُدرج فاصل فقرة في المستند في C++."
type: docs
weight: 73000
url: /ar/cpp/aspose.words/documentbuilder/writeln/
---
## DocumentBuilder::Writeln() method


يقوم بإدراج فاصل فقرة في المستند.

```cpp
void Aspose::Words::DocumentBuilder::Writeln()
```

## ملاحظات


يستدعي [InsertParagraph](../insertparagraph/).
## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::Writeln(const System::String\&) method


يدرج سلسلة نصية وفاصل فقرة في المستند.

```cpp
void Aspose::Words::DocumentBuilder::Writeln(const System::String &text)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| نص | const System::String\& | السلسلة لإدراجها في المستند. |

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

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
