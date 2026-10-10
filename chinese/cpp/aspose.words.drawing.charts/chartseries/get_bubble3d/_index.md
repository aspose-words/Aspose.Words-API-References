---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D 方法"
linktitle: "get_Bubble3D"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D 方法。指定在 C++ 中气泡图的气泡是否应应用 3D 效果。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing.charts/chartseries/get_bubble3d/
---
## ChartSeries::get_Bubble3D method


指定气泡图中的气泡是否应应用 3D 效果。

```cpp
bool Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D() override
```


## 示例



展示如何在气泡图中使用 3D 效果。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_TRUE(chart->get_Series()->idx_get(0)->get_Bubble3D());

// 为每个显示直径的气泡应用数据标签。
for (int32_t i = 0; i < 3; i++)
{
    chart->get_Series()->idx_get(0)->set_HasDataLabels(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->set_ShowBubbleSize(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->get_Font()->set_Size(12);
}

doc->Save(get_ArtifactsDir() + u"Charts.Bubble3D.docx");
```

## 另见

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
