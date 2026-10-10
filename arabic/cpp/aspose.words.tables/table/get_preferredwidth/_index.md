---
title: "طريقة Aspose::Words::Tables::Table::get_PreferredWidth"
linktitle: "get_PreferredWidth"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::get_PreferredWidth method. يحصل على أو يضبط العرض المفضل للجدول في C++."
type: docs
weight: 29000
url: /ar/cpp/aspose.words.tables/table/get_preferredwidth/
---
## Table::get_PreferredWidth method


الحصول أو تعيين العرض المفضل للجدول.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::Table::get_PreferredWidth()
```

## ملاحظات


القيمة الافتراضية هي [Auto](../../preferredwidth/auto/).

## أمثلة



يوضح كيفية ضبط جدول ليتناسب تلقائيًا مع 50٪ من عرض الصفحة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

## انظر أيضًا

* Class [PreferredWidth](../../preferredwidth/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
