---
title: "طريقة Aspose::Words::DocumentBuilder::DeleteRow"
linktitle: "DeleteRow"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::DeleteRow. تحذف صفًا من جدول في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder::DeleteRow method


يحذف صفًا من جدول.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::DocumentBuilder::DeleteRow(int32_t tableIndex, int32_t rowIndex)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| tableIndex | int32_t | فهرس الجدول. |
| rowIndex | int32_t | فهرس الصف في الجدول. |

### ReturnValue

عقدة الصف التي تم إزالتها للتو.
## ملاحظات


إذا كان المؤشر داخل الصف الذي يتم حذفه، يتم نقل المؤشر إلى الصف التالي أو إلى الفقرة التالية بعد الجدول.

إذا قمت بحذف صف من جدول يحتوي على صف واحد فقط، يتم حذف الجدول بالكامل.

بالنسبة إلى معلمات الفهرس، عندما يكون الفهرس أكبر من أو يساوي 0، فإنه يحدد فهرسًا من البداية حيث 0 هو العنصر الأول. عندما يكون الفهرس أقل من 0، فإنه يحدد فهرسًا من النهاية حيث -1 هو العنصر الأخير.

## أمثلة



يوضح كيفية حذف صف من جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, cell 2.");
builder->EndTable();

ASSERT_EQ(2, table->get_Rows()->get_Count());

// احذف الصف الأول من الجدول الأول في المستند.
builder->DeleteRow(0, 0);

ASSERT_EQ(1, table->get_Rows()->get_Count());
ASSERT_EQ(u"Row 2, cell 1.\aRow 2, cell 2.\a\a", table->GetText().Trim());
```

## انظر أيضًا

* Class [Row](../../../aspose.words.tables/row/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
