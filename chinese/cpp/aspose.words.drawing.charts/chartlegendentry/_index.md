---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry 类"
linktitle: "ChartLegendEntry"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry 类。表示图表图例条目。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class


表示图例条目。要了解更多，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

```cpp
class ChartLegendEntry : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                         public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Font](./get_font/)() | 提供对该图例条目字体格式的访问。 |
| [get_IsHidden](./get_ishidden/)() const | 获取或设置指示此条目在图表图例中是否隐藏的值。默认值为 **false**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden](./get_ishidden/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


图例条目对应特定的图表系列或趋势线。

条目的文本是系列或趋势线的名称。文本不可更改。

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
