---
title: ChartTitle
second_title: Aspose.Words for C++ API Reference
description: Provides access to the chart title properties. To learn more, visit the  documentation article.
type: docs
weight: 222
url: /cpp/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class


Provides access to the chart title properties. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartTitle : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                   public Aspose::Words::IRunAttrSource
```

## Methods

| Method | Description |
| --- | --- |
| [get_Overlay](./get_overlay/)() const | Determines whether other chart elements shall be allowed to overlap title. By default overlay is **false**. |
| [get_Show](./get_show/)() | Determines whether the title shall be shown for this chart. Default value is **true**. |
| [get_Text](./get_text/)() | Gets or sets the text of the chart title. If **null** or empty value is specified, auto generated title will be shown. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Overlay](./set_overlay/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay](./get_overlay/). |
| [set_Show](./set_show/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Setter for [Aspose::Words::Drawing::Charts::ChartTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## Examples



Shows how to insert a chart and set a title. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a chart shape with a document builder and get its chart.
SharedPtr<Shape> chartShape = builder->InsertChart(ChartType::Bar, 400, 300);
SharedPtr<Chart> chart = chartShape->get_Chart();

// Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
SharedPtr<ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");

// Set the "Show" property to "true" to make the title visible.
title->set_Show(true);

// Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
title->set_Overlay(true);

doc->Save(ArtifactsDir + u"Charts.ChartTitle.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words](../../)
