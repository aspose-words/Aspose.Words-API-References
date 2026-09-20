---
title: "Aspose::Words::Drawing::Charts::ChartXValueCollection class"
linktitle: "ChartXValueCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartXValueCollection 类。表示 C++ 中图表系列的 X 值集合。"
type: docs
weight: 18400
url: /zh/cpp/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class


表示图表系列的 X 值集合。

```cpp
class ChartXValueCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Count](./get_count/)() | 获取此集合中的项目数量。 |
| [get_FormatCode](./get_formatcode/)() | 获取或设置应用于 X 值的格式代码。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 获取或设置指定索引处的 X 值。 |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | 获取或设置指定索引处的 X 值。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | 用于 [Aspose::Words::Drawing::Charts::ChartXValueCollection::get_FormatCode](./get_formatcode/) 的设置器。 |
| static [Type](./type/)() |  |
## 备注


集合中除 **null** 之外的所有项必须具有相同的 [ValueType](../chartxvalue/get_valuetype/)。

该集合仅允许更改 X 值。要向图表系列添加或插入新值，或删除值，可使用 [ChartSeries](../chartseries/) 类的相应方法。

## 示例



展示如何获取图表系列数据。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->idx_get(0);

double minValue = std::numeric_limits<double>::max();
int32_t minValueIndex = 0;
double maxValue = std::numeric_limits<double>::lowest();
int32_t maxValueIndex = 0;

for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    // 清除所有数据点的单独格式。
    // 在柱形图中，数据点与数据值是一对一对应的。
    series->get_DataPoints()->idx_get(i)->ClearFormat();

    // 获取 Y 值。
    double yValue = series->get_YValues()->idx_get(i)->get_DoubleValue();

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// 更改最大值和最小值的颜色。
series->get_DataPoints()->idx_get(minValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series->get_DataPoints()->idx_get(maxValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Charts.GetChartSeriesData.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
