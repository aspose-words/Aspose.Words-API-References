---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection 类"
linktitle: "ChartSeriesCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection 类。表示 ChartSeries 的集合。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class


表示 [ChartSeries](../chartseries/) 的集合。欲了解更多，请访问 [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) 文档文章。

```cpp
class ChartSeriesCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&) | 向此集合添加新的 [ChartSeries](../chartseries/)。使用此方法可向任何类型的条形、柱形、折线和曲面图添加系列。 |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<bool\>\&) |  |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | 向此集合添加新的[ChartSeries](../chartseries/)。使用此方法向任何类型的散点图添加系列。 |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::DateTime\>\&, const System::ArrayPtr\<double\>\&) | 向此集合添加新的[ChartSeries](../chartseries/)。使用此方法向任何类型的面积图、雷达图和股票图添加系列。 |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | 向此集合添加新的[ChartSeries](../chartseries/)。使用此方法向任何类型的气泡图添加系列。 |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\>\&, const System::ArrayPtr\<double\>\&) | 向此集合添加新的[ChartSeries](../chartseries/)。使用此方法添加具有多级数据类别的系列。 |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&) | 向此集合添加新的[ChartSeries](../chartseries/)。使用此方法向直方图添加系列。 |
| [Clear](./clear/)() | 从此集合中移除所有[ChartSeries](../chartseries/)。 |
| [get_Count](./get_count/)() | 返回此集合中[ChartSeries](../chartseries/)的数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 返回指定索引处的[ChartSeries](../chartseries/)。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | 移除指定索引处的[ChartSeries](../chartseries/)。 |
| static [Type](./type/)() |  |

## 示例



展示如何在图表中添加和移除系列数据。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个柱状图，默认包含三个演示数据系列。
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// 每个系列有四个十进制值：分别对应四个类别。
// 四个由三根柱组成的簇将表示这些数据。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> chartData = chart->get_Series();

ASSERT_EQ(3, chartData->get_Count());

// 打印图表中每个系列的名称。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>> enumerator = chart->get_Series()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current()->get_Name() << std::endl;
    }
}

// 这些是图表中类别的名称。
System::ArrayPtr<System::String> categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});

// 我们可以为现有类别添加带有新值的系列。
// 此图表现在将包含四个由四根柱组成的簇。
chart->get_Series()->Add(u"Series 4", categories, System::MakeArray<double>({4.4, 7.0, 3.5, 2.1}));

// 也可以通过索引移除图表系列，如下所示。
// 这将移除图表自带的三个演示系列中的一个。
chartData->RemoveAt(2);

ASSERT_FALSE(chartData->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s) -> bool
{
    return s->get_Name() == u"Series 3";
}))));

// 我们也可以使用此方法一次性清除图表的所有数据。
// 在创建新图表时，这是清除所有演示数据的方法
// 在我们开始处理空白图表之前。
chartData->Clear();
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
