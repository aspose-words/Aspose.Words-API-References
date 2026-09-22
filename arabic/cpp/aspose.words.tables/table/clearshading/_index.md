---
title: "طريقة Aspose::Words::Tables::Table::ClearShading"
linktitle: "ClearShading"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Table::ClearShading. يزيل جميع التظليل على الجدول في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.tables/table/clearshading/
---
## Table::ClearShading method


يزيل جميع التظليل في الجدول.

```cpp
void Aspose::Words::Tables::Table::ClearShading()
```


## أمثلة



يظهر كيفية تطبيق حد خارجي على جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// محاذاة الجدول إلى مركز الصفحة.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// مسح أي حدود أو تظليل موجودة من الجدول.
table->ClearBorders();
table->ClearShading();

// إضافة حدود خضراء إلى الإطار الخارجي للجدول.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// ملء الخلايا بلون أخضر فاتح صلب.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## انظر أيضًا

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
