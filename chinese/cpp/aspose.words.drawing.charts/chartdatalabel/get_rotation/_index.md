---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation 方法"
linktitle: "get_Rotation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation 方法。获取或设置标签的旋转角度（以度为单位），在 C++ 中。"
type: docs
weight: 7667
url: /zh/cpp/aspose.words.drawing.charts/chartdatalabel/get_rotation/
---
## ChartDataLabel::get_Rotation method


获取或设置标签的旋转角度（以度为单位）。

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation()
```

## 备注


可接受的值范围为 -180 到 180（含），默认值为 0。

如果 [Orientation](../get_orientation/) 值为 [Horizontal](../../../aspose.words.drawing/shapetextorientation/)，则标签形状（如果存在）会随标签文本一起旋转。否则，仅旋转标签文本。

## 示例



展示如何更改数据标签的方向和旋转。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// 显示数据标签。
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// 定义数据标签形状。
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// 为整个系列设置数据标签的方向和旋转。
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// 更改第一个数据标签的方向和旋转。
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## 另见

* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
