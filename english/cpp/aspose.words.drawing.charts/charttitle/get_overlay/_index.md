---
title: Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay method
linktitle: get_Overlay
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay method. Determines whether other chart elements shall be allowed to overlap title. By default overlay is false in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.drawing.charts/charttitle/get_overlay/
---
## ChartTitle::get_Overlay method


Determines whether other chart elements shall be allowed to overlap title. By default overlay is **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay()
```


## Examples



Shows how to insert a chart and set a title. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a chart shape with a document builder and get its chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Set the "Show" property to "true" to make the title visible.
title->set_Show(true);

// Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## See Also

* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
