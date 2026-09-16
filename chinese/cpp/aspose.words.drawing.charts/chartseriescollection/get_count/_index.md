---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::get_Count 方法"
linktitle: "get_Count"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::get_Count 方法。返回此集合中 ChartSeries 的数量（C++）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.drawing.charts/chartseriescollection/get_count/
---
## ChartSeriesCollection::get_Count method


返回此集合中[ChartSeries](../../chartseries/)的数量。

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesCollection::get_Count()
```


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

* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
