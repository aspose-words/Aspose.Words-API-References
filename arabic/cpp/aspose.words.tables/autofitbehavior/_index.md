---
title: "Aspose::Words::Tables::AutoFitBehavior enum"
linktitle: "AutoFitBehavior"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::AutoFitBehavior enum. يحدد كيف يقوم Aspose.Words بإعادة تحجيم الجدول عندما تستدعي طريقة AutoFit() في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enum


يحدد كيف يقوم Aspose.Words بإعادة تحجيم الجدول عندما تستدعي طريقة [AutoFit()](../table/autofit/).

```cpp
enum class AutoFitBehavior
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| AutoFitToContents | 0 | يقوم Aspose.Words بتمكين خيار AutoFit، يزيل العرض المفضل من الجدول وجميع الخلايا ثم يُحدّث تخطيط الجدول. في الجدول الناتج، يتم تحديث عرض الخلايا لتناسب محتوى الجدول. من المحتمل أن يتقلص الجدول. |
| AutoFitToWindow | 1 | عند استخدامك لهذه القيمة، يقوم Aspose.Words بتمكين خيار AutoFit، يضبط العرض المفضل للجدول على 100٪، يزيل العروض المفضلة من جميع الخلايا ثم يُحدّث تخطيط الجدول. ونتيجة لذلك، يملأ الجدول كامل العرض المتاح وتُحدَّث عروض الخلايا لتناسب محتوى الجدول. |
| FixedColumnWidths | 2 | يقوم Aspose.Words بتعطيل خيار AutoFit ويزيل العرض المفضل من الجدول. تبقى عروض الخلايا كما هي محددة في خصائص [Width](../cellformat/get_width/). |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
