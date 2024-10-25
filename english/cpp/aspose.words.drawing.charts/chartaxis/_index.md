---
title: Aspose::Words::Drawing::Charts::ChartAxis class
linktitle: ChartAxis
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartAxis class. Represents the axis options of the chart. To learn more, visit the  documentation article in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class


Represents the axis options of the chart. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartAxis : public Aspose::Words::Drawing::Charts::Core::IDmlChartTitleHolder,
                  public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                  public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                  public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methods

| Method | Description |
| --- | --- |
| [get_AxisBetweenCategories](./get_axisbetweencategories/)() | Gets or sets a flag indicating whether the value axis crosses the category axis between categories. |
| [get_BaseTimeUnit](./get_basetimeunit/)() | Returns or sets the smallest time unit that is represented on the time category axis. |
| [get_CategoryType](./get_categorytype/)() | Gets or sets type of the category axis. |
| [get_Crosses](./get_crosses/)() | Specifies how this axis crosses the perpendicular axis. |
| [get_CrossesAt](./get_crossesat/)() | Specifies where on the perpendicular axis the axis crosses. |
| [get_DisplayUnit](./get_displayunit/)() | Specifies the scaling value of the display units for the value axis. |
| [get_Document](./get_document/)() | Returns the [Document](../../aspose.words/document/) the title holder belongs. |
| [get_Format](./get_format/)() |  |
| [get_HasMajorGridlines](./get_hasmajorgridlines/)() | Gets a flag indicating whether the axis has major gridlines. |
| [get_HasMinorGridlines](./get_hasminorgridlines/)() | Gets a flag indicating whether the axis has minor gridlines. |
| [get_Hidden](./get_hidden/)() | Gets or sets a flag indicating whether this axis is hidden or not. |
| [get_MajorTickMark](./get_majortickmark/)() | Returns or sets the major tick marks. |
| [get_MajorUnit](./get_majorunit/)() | Returns or sets the distance between major tick marks. |
| [get_MajorUnitIsAuto](./get_majorunitisauto/)() | Gets or sets a flag indicating whether default distance between major tick marks shall be used. |
| [get_MajorUnitScale](./get_majorunitscale/)() | Returns or sets the scale value for major tick marks on the time category axis. |
| [get_MinorTickMark](./get_minortickmark/)() | Returns or sets the minor tick marks for the axis. |
| [get_MinorUnit](./get_minorunit/)() | Returns or sets the distance between minor tick marks. |
| [get_MinorUnitIsAuto](./get_minorunitisauto/)() | Gets or sets a flag indicating whether default distance between minor tick marks shall be used. |
| [get_MinorUnitScale](./get_minorunitscale/)() | Returns or sets the scale value for minor tick marks on the time category axis. |
| [get_NumberFormat](./get_numberformat/)() | Returns a [ChartNumberFormat](../chartnumberformat/) object that allows defining number formats for the axis. |
| [get_ReverseOrder](./get_reverseorder/)() | Returns or sets a flag indicating whether values of axis should be displayed in reverse order, i.e. from max to min. |
| [get_Scaling](./get_scaling/)() | Provides access to the scaling options of the axis. |
| [get_TickLabels](./get_ticklabels/)() |  |
| [get_TickMarkSpacing](./get_tickmarkspacing/)() | Gets or sets the interval, at which tick marks are drawn. |
| [get_Title](./get_title/)() |  |
| [get_Type](./get_type/)() const | Returns type of the axis. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisBetweenCategories](./set_axisbetweencategories/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories](./get_axisbetweencategories/). |
| [set_BaseTimeUnit](./set_basetimeunit/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_BaseTimeUnit](./get_basetimeunit/). |
| [set_CategoryType](./set_categorytype/)(Aspose::Words::Drawing::Charts::AxisCategoryType) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_CategoryType](./get_categorytype/). |
| [set_Crosses](./set_crosses/)(Aspose::Words::Drawing::Charts::AxisCrosses) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_Crosses](./get_crosses/). |
| [set_CrossesAt](./set_crossesat/)(double) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt](./get_crossesat/). |
| [set_HasMajorGridlines](./set_hasmajorgridlines/)(bool) | Sets a flag indicating whether the axis has major gridlines. |
| [set_HasMinorGridlines](./set_hasminorgridlines/)(bool) | Sets a flag indicating whether the axis has minor gridlines. |
| [set_Hidden](./set_hidden/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden](./get_hidden/). |
| [set_MajorTickMark](./set_majortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorTickMark](./get_majortickmark/). |
| [set_MajorUnit](./set_majorunit/)(double) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnit](./get_majorunit/). |
| [set_MajorUnitIsAuto](./set_majorunitisauto/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitIsAuto](./get_majorunitisauto/). |
| [set_MajorUnitScale](./set_majorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale](./get_majorunitscale/). |
| [set_MinorTickMark](./set_minortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorTickMark](./get_minortickmark/). |
| [set_MinorUnit](./set_minorunit/)(double) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnit](./get_minorunit/). |
| [set_MinorUnitIsAuto](./set_minorunitisauto/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto](./get_minorunitisauto/). |
| [set_MinorUnitScale](./set_minorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale](./get_minorunitscale/). |
| [set_ReverseOrder](./set_reverseorder/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_ReverseOrder](./get_reverseorder/). |
| [set_TickMarkSpacing](./set_tickmarkspacing/)(int32_t) | Setter for [Aspose::Words::Drawing::Charts::ChartAxis::get_TickMarkSpacing](./get_tickmarkspacing/). |
| static [Type](./type/)() |  |

## Examples



Shows how to insert a chart and modify the appearance of its axes. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertChart(ChartType::Column, 500, 300);
SharedPtr<Chart> chart = shape->get_Chart();

// Clear the chart's demo data series to start with a clean chart.
chart->get_Series()->Clear();

// Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
chart->get_Series()->Add(u"Aspose Test Series", MakeArray<String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}),
                         MakeArray<double>({640, 320, 280, 120, 150}));

// Chart axes have various options that can change their appearance,
// such as their direction, major/minor unit ticks, and tick marks.
SharedPtr<ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(AxisCategoryType::Category);
xAxis->set_Crosses(AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(AxisTickMark::Inside);
xAxis->set_MinorTickMark(AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

SharedPtr<ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(AxisCategoryType::Automatic);
yAxis->set_Crosses(AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(AxisTickMark::Inside);
yAxis->set_MinorTickMark(AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(AxisTickLabelPosition::NextToAxis);

// Column charts do not have a Z-axis.
ASSERT_TRUE(chart->get_AxisZ() == nullptr);

doc->Save(ArtifactsDir + u"Charts.AxisProperties.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
