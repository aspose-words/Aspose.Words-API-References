---
title: "طريقة Aspose::Words::Tables::Table::get_StyleOptions"
linktitle: "get_StyleOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Table::get_StyleOptions. يحصل أو يضبط علامات البت التي تحدد كيفية تطبيق نمط الجدول على هذا الجدول في C++."
type: docs
weight: 37000
url: /ar/cpp/aspose.words.tables/table/get_styleoptions/
---
## Table::get_StyleOptions method


الحصول أو تعيين أعلام البت التي تحدد كيفية تطبيق نمط الجدول على هذا الجدول.

```cpp
Aspose::Words::Tables::TableStyleOptions Aspose::Words::Tables::Table::get_StyleOptions()
```


## أمثلة



يوضح كيفية إنشاء جدول جديد مع تطبيق نمط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// يجب أن ندخل صفًا واحدًا على الأقل قبل ضبط أي تنسيق للجدول.
builder->InsertCell();

// حدد نمط الجدول المستخدم بناءً على معرف النمط.
// لاحظ أن ليس جميع أنماط الجداول متاحة عند الحفظ بتنسيق .doc.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// طبق النمط جزئيًا على ميزات الجدول بناءً على الشروط، ثم أنشئ الجدول.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```

## انظر أيضًا

* Enum [TableStyleOptions](../../tablestyleoptions/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
