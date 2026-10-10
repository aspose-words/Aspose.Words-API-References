---
title: "طريقة Aspose::Words::Tables::Table::get_AllowAutoFit"
linktitle: "get_AllowAutoFit"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Table::get_AllowAutoFit. يسمح لـ Microsoft Word و Aspose.Words بإعادة تحجيم خلايا الجدول تلقائيًا لتناسب محتوياتها في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.tables/table/get_allowautofit/
---
## Table::get_AllowAutoFit method


يسمح لـ Microsoft Word و Aspose.Words بإعادة تحجيم الخلايا في جدول تلقائيًا لتناسب محتواها.

```cpp
bool Aspose::Words::Tables::Table::get_AllowAutoFit()
```

## ملاحظات


القيمة الافتراضية هي **true**.

## أمثلة



يظهر كيفية تمكين/تعطيل إعادة تحجيم خلايا الجدول تلقائيًا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(100));
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->EndRow();
builder->EndTable();

// قم بتعيين الخاصية "AllowAutoFit" إلى "false" لجعل الجدول يحافظ على الأبعاد
// جميع صفوفه وخلاياه، وقص المحتويات إذا أصبحت كبيرة جدًا لتناسب.
// قم بتعيين الخاصية "AllowAutoFit" إلى "true" للسماح للجدول بتغيير عرض وارتفاع خلاياه
// لتستوعب محتوياتها.
table->set_AllowAutoFit(allowAutoFit);

doc->Save(get_ArtifactsDir() + u"Table.AllowAutoFitOnTable.html");
```

## انظر أيضًا

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
