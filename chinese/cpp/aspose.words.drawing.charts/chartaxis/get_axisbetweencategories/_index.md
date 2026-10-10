---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories 方法"
linktitle: "get_AxisBetweenCategories"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories 方法。获取或设置一个标志，指示值轴是否在 C++ 中跨越类别轴之间的类别。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing.charts/chartaxis/get_axisbetweencategories/
---
## ChartAxis::get_AxisBetweenCategories method


获取或设置一个标志，指示值轴是否在类别之间跨越类别轴。

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories()
```


## 示例



展示如何让图表轴在自定义位置交叉。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// 对于柱状图，Y 轴默认在零处交叉，
// 这意味着所有低于零的值的柱子向下延伸，以表示负值。
// 我们可以为 Y 轴交叉设置不同的值。在本例中，我们将其设置为 3。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisX();
axis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Custom);
axis->set_CrossesAt(3);
axis->set_AxisBetweenCategories(true);

doc->Save(get_ArtifactsDir() + u"Charts.AxisCross.docx");
```

## 另见

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
