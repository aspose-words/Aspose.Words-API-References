---
title: "Aspose::Words::Drawing::Charts::Chart class"
linktitle: "مخطط"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Drawing::Charts::Chart. توفر الوصول إلى خصائص شكل المخطط. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing.charts/chart/
---
## Chart class


يوفر الوصول إلى خصائص شكل المخطط. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class Chart : public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Axes](./get_axes/)() | يحصل على مجموعة جميع محاور هذا المخطط. |
| [get_AxisX](./get_axisx/)() | يوفر الوصول إلى خصائص المحور X الأساسي للمخطط. |
| [get_AxisY](./get_axisy/)() | يوفر الوصول إلى خصائص المحور Y الأساسي للمخطط. |
| [get_AxisZ](./get_axisz/)() | يوفر الوصول إلى خصائص المحور Z للمخطط. |
| [get_DataTable](./get_datatable/)() | يوفر الوصول إلى خصائص جدول البيانات لهذا المخطط. يمكن إظهار جدول البيانات باستخدام خاصية [Show](../chartdatatable/get_show/). |
| [get_Format](./get_format/)() | يوفر الوصول إلى تنسيق التعبئة والخط للمخطط. |
| [get_Legend](./get_legend/)() | يوفر الوصول إلى خصائص وسيلة إيضاح المخطط. |
| [get_Series](./get_series/)() | يوفر الوصول إلى مجموعة السلاسل. |
| [get_SeriesGroups](./get_seriesgroups/)() | يوفر الوصول إلى مجموعة مجموعات السلاسل لهذا المخطط. |
| [get_SourceFullName](./get_sourcefullname/)() | يحصل على مسار واسم ملف xls/xlsx المرتبط بهذا المخطط. |
| [get_Style](./get_style/)() | يحصل على نمط المخطط. |
| [get_Title](./get_title/)() | يوفر الوصول إلى خصائص عنوان المخطط. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Drawing::Charts::Chart::get_SourceFullName](./get_sourcefullname/). |
| [set_Style](./set_style/)(Aspose::Words::Drawing::Charts::ChartStyle) | يضبط نمط المخطط. |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية إدراج مخطط وتعيين عنوان.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج شكل مخطط باستخدام منشئ المستند واحصل على مخططه.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// استخدم خاصية "Title" لإعطاء مخططنا عنوانًا، يظهر في أعلى وسط منطقة المخطط.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// اضبط خاصية "Show" إلى "true" لجعل العنوان مرئيًا.
title->set_Show(true);

// اضبط خاصية "Overlay" إلى "true" لمنح عناصر المخطط الأخرى مساحة أكبر بالسماح لها بتغطية العنوان.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
