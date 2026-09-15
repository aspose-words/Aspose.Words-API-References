---
title: "Aspose::Words::Tables::RowFormat class"
linktitle: "RowFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::RowFormat class. يمثل جميع تنسيقات صف الجدول. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.tables/rowformat/
---
## RowFormat class


يمثل كل تنسيق صف الجدول. لمعرفة المزيد، زر مقالة الوثائق [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class RowFormat : public Aspose::Words::IBorderAttrSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | يعيد تنسيق الصف إلى الإعدادات الافتراضية. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | صحيح إذا كان مسموحًا للنص في صف الجدول أن ينقسم عبر فاصل صفحة. |
| [get_Borders](./get_borders/)() | يحصل على مجموعة حدود الخلايا الافتراضية للصف. |
| [get_HeadingFormat](./get_headingformat/)() | صحيح إذا تم تكرار الصف كعنوان جدول في كل صفحة عندما يمتد الجدول على أكثر من صفحة. |
| [get_Height](./get_height/)() | يحصل أو يعيّن ارتفاع صف الجدول بالنقاط. |
| [get_HeightRule](./get_heightrule/)() | يحصل أو يعيّن القاعدة لتحديد ارتفاع صف الجدول. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | محدد لـ [Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_HeadingFormat](./set_headingformat/)(bool) | محدد لـ [Aspose::Words::Tables::RowFormat::get_HeadingFormat](./get_headingformat/). |
| [set_Height](./set_height/)(double) | دالة الضبط لـ [Aspose::Words::Tables::RowFormat::get_Height](./get_height/). |
| [set_HeightRule](./set_heightrule/)(Aspose::Words::HeightRule) | دالة الضبط لـ [Aspose::Words::Tables::RowFormat::get_HeightRule](./get_heightrule/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية بناء جدول بحدود مخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// تعيين خيارات تنسيق الجدول لمنشئ المستند
// سيتم تطبيقها على كل صف وخلية نضيفها به.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// تغيير التنسيق سيطبقه على الخلية الحالية،
// وأي خلايا جديدة ننشئها باستخدام المنشئ لاحقًا.
// هذا لن يؤثر على الخلايا التي أضفناها مسبقًا.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// زد ارتفاع الصف لتناسب النص العمودي.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


يوضح كيفية تعديل تنسيق الصفوف والخلايا في جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"City");
builder->InsertCell();
builder->Write(u"Country");
builder->EndRow();
builder->InsertCell();
builder->Write(u"London");
builder->InsertCell();
builder->Write(u"U.K.");
builder->EndTable();

// استخدم خاصية "RowFormat" للصف الأول لتعديل التنسيق
// لمحتويات جميع الخلايا في هذا الصف.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// استخدم خاصية "CellFormat" للخلية الأولى في الصف الأخير لتعديل تنسيق محتويات تلك الخلية.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


يوضح كيفية تعديل تنسيق صف جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// استخدم خاصية "RowFormat" للصف الأول لتعيين تنسيق يغيّر مظهر الصف بالكامل.
System::SharedPtr<Aspose::Words::Tables::Row> firstRow = table->get_FirstRow();
firstRow->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::None);
firstRow->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
firstRow->get_RowFormat()->set_AllowBreakAcrossPages(true);

doc->Save(get_ArtifactsDir() + u"Table.RowFormat.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
