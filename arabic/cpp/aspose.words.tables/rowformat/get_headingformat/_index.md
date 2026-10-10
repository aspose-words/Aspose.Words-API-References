---
title: "طريقة Aspose::Words::Tables::RowFormat::get_HeadingFormat"
linktitle: "get_HeadingFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::RowFormat::get_HeadingFormat. صحيح إذا تم تكرار الصف كعنوان جدول في كل صفحة عندما يمتد الجدول على أكثر من صفحة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.tables/rowformat/get_headingformat/
---
## RowFormat::get_HeadingFormat method


صحيح إذا تم تكرار الصف كعنوان جدول في كل صفحة عندما يمتد الجدول على أكثر من صفحة.

```cpp
bool Aspose::Words::Tables::RowFormat::get_HeadingFormat()
```


## أمثلة



يعرض كيفية بناء جدول يحتوي على صفوف تتكرر في كل صفحة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// أي صفوف يتم إدراجها بينما يتم تعيين علم "HeadingFormat" إلى "true"
// ستظهر في أعلى الجدول في كل صفحة يمتد إليها.
builder->get_RowFormat()->set_HeadingFormat(true);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_CellFormat()->set_Width(100);
builder->InsertCell();
builder->Write(u"Heading row 1");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Heading row 2");
builder->EndRow();

builder->get_CellFormat()->set_Width(50);
builder->get_ParagraphFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeadingFormat(false);

// أضف عددًا كافيًا من الصفوف حتى يمتد الجدول على صفحتين.
for (int32_t i = 0; i < 50; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 1.", table->get_Rows()->get_Count()));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 2.", table->get_Rows()->get_Count()));
    builder->EndRow();
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableSetHeadingRow.docx");
```

## انظر أيضًا

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
