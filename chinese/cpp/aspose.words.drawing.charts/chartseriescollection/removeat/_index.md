---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::RemoveAt 方法"
linktitle: "RemoveAt"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::RemoveAt 方法。删除指定索引处的 ChartSeries（在 C++ 中）。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.drawing.charts/chartseriescollection/removeat/
---
## ChartSeriesCollection::RemoveAt method


删除指定索引处的 [ChartSeries](../../chartseries/)。

```cpp
void Aspose::Words::Drawing::Charts::ChartSeriesCollection::RemoveAt(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 要删除的 [ChartSeries](../../chartseries/) 的零基索引。 |

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
