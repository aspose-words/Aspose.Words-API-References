---
title: "فئة Aspose::Words::Tables::CellFormat"
linktitle: "CellFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Tables::CellFormat. تمثل جميع تنسيقات خلية الجدول. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.tables/cellformat/
---
## CellFormat class


يمثل كل تنسيق خلية الجدول. لمعرفة المزيد، زر مقالة الوثائق [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class CellFormat : public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | يعيد تنسيق الخلية إلى الإعدادات الافتراضية. لا يغيّر عرض الخلية. |
| [get_Borders](./get_borders/)() | يحصل على مجموعة حدود الخلية. |
| [get_BottomPadding](./get_bottompadding/)() | يرجع أو يضبط مقدار المسافة (بالنقاط) لإضافتها أسفل محتويات الخلية. |
| [get_FitText](./get_fittext/)() | إذا كان **true**، يضبط النص داخل الخلية، مضغًا كل فقرة إلى عرض الخلية. |
| [get_HideMark](./get_hidemark/)() | يرجع رؤية علامة الخلية. |
| [get_HorizontalMerge](./get_horizontalmerge/)() | يحدد كيفية دمج الخلية أفقيًا مع خلايا أخرى في الصف. |
| [get_LeftPadding](./get_leftpadding/)() | يرجع أو يضبط مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتويات الخلية. |
| [get_Orientation](./get_orientation/)() | يرجع أو يضبط اتجاه النص في خلية الجدول. |
| [get_PreferredWidth](./get_preferredwidth/)() | يرجع أو يضبط العرض المفضل للخلية. |
| [get_RightPadding](./get_rightpadding/)() | يرجع أو يضبط مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتويات الخلية. |
| [get_Shading](./get_shading/)() | يرجع كائن [Shading](../../aspose.words/shading/) الذي يشير إلى تنسيق التظليل للخلية. |
| [get_TopPadding](./get_toppadding/)() | يرجع أو يضبط مقدار المسافة (بالنقاط) لإضافتها فوق محتويات الخلية. |
| [get_VerticalAlignment](./get_verticalalignment/)() | يرجع أو يضبط محاذاة النص العمودية في الخلية. |
| [get_VerticalMerge](./get_verticalmerge/)() | يحدد كيفية دمج الخلية مع خلايا أخرى عموديًا. |
| [get_Width](./get_width/)() | يحصل على عرض الخلية بالنقاط. |
| [get_WrapText](./get_wraptext/)() | إذا كان **true**، قم بلف النص للخلية. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_BottomPadding](./get_bottompadding/). |
| [set_FitText](./set_fittext/)(bool) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_FitText](./get_fittext/). |
| [set_HideMark](./set_hidemark/)(bool) | يضبط رؤية علامة الخلية. |
| [set_HorizontalMerge](./set_horizontalmerge/)(Aspose::Words::Tables::CellMerge) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_HorizontalMerge](./get_horizontalmerge/). |
| [set_LeftPadding](./set_leftpadding/)(double) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_LeftPadding](./get_leftpadding/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::TextOrientation) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_Orientation](./get_orientation/). |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_PreferredWidth](./get_preferredwidth/). |
| [set_RightPadding](./set_rightpadding/)(double) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_TopPadding](./get_toppadding/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_VerticalAlignment](./get_verticalalignment/). |
| [set_VerticalMerge](./set_verticalmerge/)(Aspose::Words::Tables::CellMerge) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_VerticalMerge](./get_verticalmerge/). |
| [set_Width](./set_width/)(double) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_Width](./get_width/). |
| [set_WrapText](./set_wraptext/)(bool) | المحدد لـ [Aspose::Words::Tables::CellFormat::get_WrapText](./get_wraptext/). |
| [SetPaddings](./setpaddings/)(double, double, double, double) | يضبط مقدار المسافة (بالنقاط) لإضافتها إلى اليسار/الأعلى/اليمين/الأسفل لمحتويات الخلية. |
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


يعرض كيفية تعديل تنسيق خلية جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

// استخدم خاصية "CellFormat" للخلية لضبط التنسيق الذي يغيّر مظهر تلك الخلية.
firstCell->get_CellFormat()->set_Width(30);
firstCell->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
firstCell->get_CellFormat()->get_Shading()->set_ForegroundPatternColor(System::Drawing::Color::get_LightGreen());

doc->Save(get_ArtifactsDir() + u"Table.CellFormat.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
