---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle 方法"
linktitle: "get_FirstSliceAngle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle 方法。获取或设置父饼图第一切片的角度（以度为单位）（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.drawing.charts/chartseriesgroup/get_firstsliceangle/
---
## ChartSeriesGroup::get_FirstSliceAngle method


获取或设置父饼图第一块的角度（以度为单位）。

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle()
```

## 备注


适用于 [Pie](../../chartseriestype/)、[Pie3D](../../chartseriestype/) 和 [Doughnut](../../chartseriestype/) 类型的系列组。

可接受值的范围为 0 到 360（含），默认值为 0。

## 示例



展示如何创建和格式化环形图。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, 400, 400);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// 删除默认生成的系列。
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({4, 2, 5}));

// 格式化环形图。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_DoughnutHoleSize(10);
seriesGroup->set_FirstSliceAngle(270);

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChart.docx");
```

## 另见

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
