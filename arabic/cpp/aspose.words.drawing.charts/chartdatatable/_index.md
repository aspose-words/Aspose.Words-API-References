---
title: "Aspose::Words::Drawing::Charts::ChartDataTable class"
linktitle: "ChartDataTable"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataTable class. يسمح بتحديد خصائص جدول بيانات المخطط في C++."
type: docs
weight: 9500
url: /ar/cpp/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class


يسمح بتحديد خصائص جدول بيانات المخطط.

```cpp
class ChartDataTable : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Font](./get_font/)() | يوفر الوصول إلى تنسيق الخط لجدول البيانات. |
| [get_Format](./get_format/)() | يوفر الوصول إلى تعبئة خلفية النص وتنسيق حدود جدول البيانات. |
| [get_HasHorizontalBorder](./get_hashorizontalborder/)() const | يحصل أو يعيّن علامة تشير إلى ما إذا كان الحد الأفقي لجدول البيانات معروضًا. القيمة الافتراضية هي **true**. |
| [get_HasLegendKeys](./get_haslegendkeys/)() const | يحصل أو يعيّن علامة تشير إلى ما إذا كانت مفاتيح الوسيلة المعروضة في جدول البيانات. القيمة الافتراضية هي **true**. |
| [get_HasOutlineBorder](./get_hasoutlineborder/)() const | يحصل أو يعيّن علامة تشير إلى ما إذا كان الحد الخارجي، أي الحد حول أسماء السلاسل والفئات، معروضًا. القيمة الافتراضية هي **true**. |
| [get_HasVerticalBorder](./get_hasverticalborder/)() const | يحصل أو يعيّن علامة تشير إلى ما إذا كان الحد العمودي لجدول البيانات معروضًا. القيمة الافتراضية هي **true**. |
| [get_Show](./get_show/)() const | يحصل أو يعيّن علامة تشير إلى ما إذا كان سيتم عرض جدول البيانات للمخطط. القيمة الافتراضية هي **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_HasHorizontalBorder](./set_hashorizontalborder/)(bool) | محدد لـ [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasHorizontalBorder](./get_hashorizontalborder/). |
| [set_HasLegendKeys](./set_haslegendkeys/)(bool) | محدد لـ [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasLegendKeys](./get_haslegendkeys/). |
| [set_HasOutlineBorder](./set_hasoutlineborder/)(bool) | محدد لـ [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder](./get_hasoutlineborder/). |
| [set_HasVerticalBorder](./set_hasverticalborder/)(bool) | محدد لـ [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasVerticalBorder](./get_hasverticalborder/). |
| [set_Show](./set_show/)(bool) | محدد لـ [Aspose::Words::Drawing::Charts::ChartDataTable::get_Show](./get_show/). |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية عرض جدول البيانات مع بيانات سلسلة المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();
auto xValues = System::MakeArray<double>({2020, 2021, 2022, 2023});
series->Add(u"Series1", xValues, System::MakeArray<double>({5, 11, 2, 7}));
series->Add(u"Series2", xValues, System::MakeArray<double>({6, 5.5, 7, 7.8}));
series->Add(u"Series3", xValues, System::MakeArray<double>({10, 8, 7, 9}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataTable> dataTable = chart->get_DataTable();
dataTable->set_Show(true);

dataTable->set_HasLegendKeys(false);
dataTable->set_HasHorizontalBorder(false);
dataTable->set_HasVerticalBorder(false);
dataTable->set_HasOutlineBorder(false);

dataTable->get_Font()->set_Italic(true);
dataTable->get_Format()->get_Stroke()->set_Weight(1);
dataTable->get_Format()->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDot);
dataTable->get_Format()->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());

doc->Save(get_ArtifactsDir() + u"Charts.DataTable.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
