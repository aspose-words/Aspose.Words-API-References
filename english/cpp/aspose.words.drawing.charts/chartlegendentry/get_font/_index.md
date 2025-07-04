---
title: Aspose::Words::Drawing::Charts::ChartLegendEntry::get_Font method
linktitle: get_Font
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartLegendEntry::get_Font method. Provides access to the font formatting of this legend entry in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.drawing.charts/chartlegendentry/get_font/
---
## ChartLegendEntry::get_Font method


Provides access to the font formatting of this legend entry.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartLegendEntry::get_Font()
```


## Examples



Shows how to work with a legend font. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// Set default font size all legend entries.
chartLegend->get_Font()->set_Size(14);
// Change font for specific legend entry.
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// Get legend entry for chart series.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## See Also

* Class [Font](../../../aspose.words/font/)
* Class [ChartLegendEntry](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
