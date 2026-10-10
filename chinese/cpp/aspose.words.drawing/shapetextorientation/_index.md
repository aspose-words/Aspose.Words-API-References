---
title: "Aspose::Words::Drawing::ShapeTextOrientation 枚举"
linktitle: "ShapeTextOrientation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeTextOrientation 枚举。指定 C++ 中形状中文本的方向。"
type: docs
weight: 37500
url: /zh/cpp/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enum


指定形状中文本的方向。

```cpp
enum class ShapeTextOrientation
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Horizontal | 0 | 文本水平排列 (lr-tb)。 |
| 向下 | 1 | 文本向右旋转 90 度，以从上到下显示 (tb-rl)。 |
| 向上 | 2 | 文本向左旋转 90 度，以从下到上显示 (bt-lr)。 |
| VerticalFarEast | 3 | 东亚字符垂直显示，其他文本向右旋转 90 度，以从上到下显示 (tb-rl-v)。 |
| VerticalRotatedFarEast | 4 | 东亚字符垂直显示，其他文本向右旋转 90 度，以从上到下垂直显示，然后水平从左到右排列 (tb-lr-v)。 |
| WordArtVertical | 5 | 文本垂直排列，字母上下堆叠。 |
| WordArtVerticalRightToLeft | 6 | 文本垂直排列，字母上下堆叠，然后水平从右到左。 |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
