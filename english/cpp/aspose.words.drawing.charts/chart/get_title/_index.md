---
title: get_Title
second_title: Aspose.Words for C++ API Reference
description: Provides access to the chart title properties.
type: docs
weight: 79
url: /cpp/aspose.words.drawing.charts/chart/get_title/
---
## Chart::get_Title method


Provides access to the chart title properties.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> Aspose::Words::Drawing::Charts::Chart::get_Title()
```


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

* Class [ChartTitle](../../charttitle/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
