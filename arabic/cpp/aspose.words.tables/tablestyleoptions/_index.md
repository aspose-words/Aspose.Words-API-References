---
title: "Aspose::Words::Tables::TableStyleOptions enum"
linktitle: "TableStyleOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::TableStyleOptions enum. يحدد كيفية تطبيق نمط الجدول على جدول في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enum


يحدد كيفية تطبيق نمط الجدول على الجدول.

```cpp
enum class TableStyleOptions
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | لم يتم تطبيق أي تنسيق لنمط الجدول. |
| FirstRow | 32 | طبق تنسيقًا شرطيًا للصف الأول. |
| LastRow | 64 | طبق تنسيقًا شرطيًا للصف الأخير. |
| FirstColumn | 128 | طبق تنسيقًا شرطيًا للعمود الأول 1. |
| LastColumn | 256 | طبق تنسيقًا شرطيًا للعمود الأخير. |
| RowBands | 512 | طبق تنسيقًا شرطيًا لتقليب الصفوف. |
| ColumnBands | 1024 | طبق تنسيقًا شرطيًا لتقليب الأعمدة. |
| Default2003 | n/a | [Row](../row/) وتطبيق تقليب الأعمدة. هذا هو الإعداد الافتراضي لبرنامج Microsoft Word للنسق القديمة مثل DOC وWML وRTF. |
| افتراضي | n/a | هذه هي الإعدادات الافتراضية لبرنامج Microsoft Word. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
