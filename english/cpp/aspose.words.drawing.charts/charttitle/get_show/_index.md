---
title: get_Show
second_title: Aspose.Words for C++ API Reference
description: Determines whether the title shall be shown for this chart. Default value is true.
type: docs
weight: 27
url: /cpp/aspose.words.drawing.charts/charttitle/get_show/
---
## ChartTitle::get_Show method


Determines whether the title shall be shown for this chart. Default value is **true**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartTitle::get_Show()
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

* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words](../../../)
