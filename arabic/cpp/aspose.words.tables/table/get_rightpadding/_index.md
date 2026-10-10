---
title: "Aspose::Words::Tables::Table::get_RightPadding طريقة"
linktitle: "get_RightPadding"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::get_RightPadding method. يحصل على أو يضبط مقدار المسافة (بالنقاط) التي تُضاف إلى يمين محتويات الخلايا في C++."
type: docs
weight: 32000
url: /ar/cpp/aspose.words.tables/table/get_rightpadding/
---
## Table::get_RightPadding method


الحصول أو تعيين مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتويات الخلايا.

```cpp
double Aspose::Words::Tables::Table::get_RightPadding()
```


## أمثلة



يوضح كيفية تكوين حشو المحتوى في جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndTable();

// لكل خلية في الجدول، اضبط المسافة بين محتواها وكل أحد حدودها.
// سيحافظ هذا الجدول على الحد الأدنى لمسافة الحشو عن طريق التفاف النص.
table->set_LeftPadding(30);
table->set_RightPadding(60);
table->set_TopPadding(10);
table->set_BottomPadding(90);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(250));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## انظر أيضًا

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
