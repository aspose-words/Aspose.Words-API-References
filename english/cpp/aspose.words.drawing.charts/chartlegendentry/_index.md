---
title: ChartLegendEntry
second_title: Aspose.Words for C++ API Reference
description: Represents a chart legend entry. To learn more, visit the  documentation article.
type: docs
weight: 144
url: /cpp/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class


Represents a chart legend entry. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartLegendEntry : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                         public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Methods

| Method | Description |
| --- | --- |
| [get_Font](./get_font/)() | Provides access to the font formatting of this legend entry. |
| [get_IsHidden](./get_ishidden/)() const | Gets a value indicating whether this entry is hidden in the chart legend. The default value is **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Sets a value indicating whether this entry is hidden in the chart legend. The default value is **false**. |
| static [Type](./type/)() |  |
## Remarks


A legend entry corresponds to a specific chart series or trendline.

The text of the entry is the name of the series or trendline. The text cannot be changed.

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words](../../)
