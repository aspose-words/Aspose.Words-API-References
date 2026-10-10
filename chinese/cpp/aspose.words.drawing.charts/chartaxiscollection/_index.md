---
title: "Aspose::Words::Drawing::Charts::ChartAxisCollection class"
linktitle: "ChartAxisCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartAxisCollection class. 表示 C++ 中的图表轴集合。"
type: docs
weight: 5500
url: /zh/cpp/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class


表示图表坐标轴的集合。

```cpp
class ChartAxisCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Count](./get_count/)() | 获取此集合中轴的数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 获取指定索引处的轴。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## 示例



展示如何使用轴集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 隐藏主 Y 轴和次 Y 轴上的主网格线。
for (auto&& axis : System::IterateOver(chart->get_Axes()))
{
    if (axis->get_Type() == Aspose::Words::Drawing::Charts::ChartAxisType::Value)
    {
        axis->set_HasMajorGridlines(false);
    }
}

doc->Save(get_ArtifactsDir() + u"Charts.AxisCollection.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
