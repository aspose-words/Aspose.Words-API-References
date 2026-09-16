---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale 方法"
linktitle: "get_BubbleScale"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale method. 获取或设置气泡的大小，作为其默认大小的百分比（C++）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.drawing.charts/chartseriesgroup/get_bubblescale/
---
## ChartSeriesGroup::get_BubbleScale method


获取或设置气泡的大小，作为其默认大小的百分比。

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale()
```

## 备注


仅适用于 [Bubble](../../chartseriestype/) 和 [Bubble3D](../../chartseriestype/) 类型的系列组。

可接受值的范围为 0 到 300（含）。默认值为 100。

## 示例



展示如何设置气泡的大小。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个 3D 气泡图表。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// 将气泡比例设置为 200%。
seriesGroup->set_BubbleScale(200);

doc->Save(get_ArtifactsDir() + u"Charts.BubbleScale.docx");
```

## 另见

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
