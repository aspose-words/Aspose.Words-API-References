---
title: "Aspose::Words::Tables::Table::AutoFit طريقة"
linktitle: "AutoFit"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::AutoFit طريقة. يعيد تحجيم الجدول والخلايا وفقًا للسلوك المحدد للملاءمة التلقائية في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.tables/table/autofit/
---
## Table::AutoFit method


يعيد تحجيم الجدول والخلايا وفقًا لسلوك الملاءمة التلقائي المحدد.

```cpp
void Aspose::Words::Tables::Table::AutoFit(Aspose::Words::Tables::AutoFitBehavior behavior)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| السلوك | Aspose::Words::Tables::AutoFitBehavior | يحدد كيفية ملاءمة الجدول تلقائيًا. |
## ملاحظات


هذه الطريقة تحاكي الأوامر المتاحة في قائمة الملاءمة التلقائية للجدول في Microsoft Word. الأوامر المتاحة هي "Auto Fit to Contents"، "Auto Fit to Window" و "Fixed Column Width". في Microsoft Word تقوم هذه الأوامر بتعيين خصائص الجدول ذات الصلة ثم تحديث تخطيط الجدول وتقوم Aspose.Words بنفس العملية لك.

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

* Enum [AutoFitBehavior](../../autofitbehavior/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
