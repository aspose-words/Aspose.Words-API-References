---
title: "Aspose::Words::Drawing::Charts::ChartDataPointCollection 类"
linktitle: "ChartDataPointCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartDataPointCollection 类。表示 ChartDataPoint 的集合。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.drawing.charts/chartdatapointcollection/
---
## ChartDataPointCollection class


表示 [ChartDataPoint](../chartdatapoint/) 的集合。欲了解更多，请访问 [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) 文档文章。

```cpp
class ChartDataPointCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormat](./clearformat/)() | 清除此集合中所有 [ChartDataPoint](../chartdatapoint/) 的格式。 |
| [CopyFormat](./copyformat/)(int32_t, int32_t) | 将格式从源数据点复制到目标数据点。 |
| [get_Count](./get_count/)() | 返回此集合中 [ChartDataPoint](../chartdatapoint/) 的数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [HasDefaultFormat](./hasdefaultformat/)(int32_t) | 获取一个标志，指示指定索引处的数据点是否具有默认格式。 |
| [idx_get](./idx_get/)(int32_t) | 返回指定索引处的 [ChartDataPoint](../chartdatapoint/)。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
