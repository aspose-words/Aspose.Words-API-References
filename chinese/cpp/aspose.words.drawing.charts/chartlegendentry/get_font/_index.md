---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry::get_Font 方法"
linktitle: "get_Font"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry::get_Font 方法。提供对该图例项字体格式的访问（在 C++ 中）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing.charts/chartlegendentry/get_font/
---
## ChartLegendEntry::get_Font method


提供对该图例条目字体格式的访问。

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartLegendEntry::get_Font()
```


## 示例



展示如何使用图例字体。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// 设置所有图例条目的默认字体大小。
chartLegend->get_Font()->set_Size(14);
// 更改特定图例条目的字体。
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// 获取图表系列的图例条目。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## 另见

* Class [Font](../../../aspose.words/font/)
* Class [ChartLegendEntry](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
