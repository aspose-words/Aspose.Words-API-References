---
title: Aspose::Words::Drawing::Charts::ChartStyle enum
linktitle: ChartStyle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartStyle enum. Specifies predefined styles of a chart in C++.'
type: docs
weight: 27875
url: /cpp/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enum


Specifies predefined styles of a chart.

```cpp
enum class ChartStyle
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Normal | 0 | Represents the default chart style. |
| Muted | 1 | A style with muted colors. |
| Saturated | 2 | A style with more saturated colors. |
| Shaded | 3 | A style with shaded data points. |
| Flat | 4 | A style with flat data points without gradient. |
| Shadowed | 5 | A style with data points having a shadow. |
| Gradient | 6 | A style with gradient fill of data points. |
| Original | 7 | A style with an original appearance of a chart. |
| Transparent1 | 8 | A style with transparent data points. |
| Transparent2 | 9 | A style with transparent data points. |
| Outline | 10 | A style with data points having no fill, but only an outline. |
| OutlineBlack | 11 | A style with black chart background, in which data points have no fill, but only an outline. |
| Black | 12 | A style with black chart background. |
| Grey | 13 | A style with gray gradient chart background. |
| Blue | 14 | A style with blue chart background. |
| ShadedPlot | 15 | A style, in which the plot area is shaded. |


## Examples



Shows how to set and get chart style. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a chart in the Black style.
builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 250, Aspose::Words::Drawing::Charts::ChartStyle::Black);

doc->Save(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

// Get a chart to update.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Get the chart style.
ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartStyle::Black, chart->get_Style());
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
