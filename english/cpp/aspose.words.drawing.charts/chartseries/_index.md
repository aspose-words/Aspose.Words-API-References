---
title: Aspose::Words::Drawing::Charts::ChartSeries class
linktitle: ChartSeries
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeries class. Represents chart series properties. To learn more, visit the  documentation article in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class


Represents chart series properties. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartSeries : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                    public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Adds the specified X value to the chart series. If the series supports Y values and bubble sizes, they will be empty for the X value. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Adds the specified X and Y values to the chart series. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Adds the specified X value, Y value and bubble size to the chart series. |
| [Clear](./clear/)() | Removes all data values from the chart series. Format of all individual data points and data labels is cleared. |
| [ClearValues](./clearvalues/)() | Removes all data values from the chart series with preserving the format of the data points and data labels. |
| [CopyFormatFrom](./copyformatfrom/)(int32_t) | Copies default data point format from the data point with the specified index. |
| [get_Bubble3D](./get_bubble3d/)() override | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [get_BubbleSizes](./get_bubblesizes/)() | Gets a collection of bubble sizes for this chart series. |
| [get_DataLabels](./get_datalabels/)() | Specifies the settings for the data labels for the entire series. |
| [get_DataPoints](./get_datapoints/)() const | Returns a collection of formatting objects for all data points in this series. |
| [get_Explosion](./get_explosion/)() override | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [get_Format](./get_format/)() | Provides access to fill and line formatting of the series. |
| [get_HasDataLabels](./get_hasdatalabels/)() const | Gets or sets a flag indicating whether data labels are displayed for the series. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [get_LegendEntry](./get_legendentry/)() | Gets a legend entry for this chart series. |
| [get_Marker](./get_marker/)() override | Specifies a data marker. Marker is automatically created when requested. |
| [get_Name](./get_name/)() | Gets the name of the series, if name is not set explicitly it is generated using index. By default returns Series plus one based index. |
| [get_SeriesType](./get_seriestype/)() | Gets the type of this chart series. |
| [get_Smooth](./get_smooth/)() const | Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines. |
| [get_XValues](./get_xvalues/)() | Gets a collection of X values for this chart series. |
| [get_YValues](./get_yvalues/)() | Gets a collection of Y values for this chart series. |
| [GetType](./gettype/)() const override |  |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Inserts the specified X value into the chart series at the specified index. If the series supports Y values and bubble sizes, they will be empty for the X value. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Inserts the specified X and Y values into the chart series at the specified index. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Inserts the specified X value, Y value and bubble size into the chart series at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Removes the X value, Y value, and bubble size, if supported, from the chart series at the specified index. The corresponding data point and data label are also removed. |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Setter for [Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D](./get_bubble3d/). |
| [set_Explosion](./set_explosion/)(int32_t) override | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [set_HasDataLabels](./set_hasdatalabels/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels](./get_hasdatalabels/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [set_Name](./set_name/)(const System::String\&) | Sets the name of the series, if name is not set explicitly it is generated using index. By default returns Series plus one based index. |
| [set_Smooth](./set_smooth/)(bool) | Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines. |
| static [Type](./type/)() |  |
## See Also

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
