---
title: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class"
linktitle: "BubbleSizeCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::BubbleSizeCollection 类。表示 C++ 中图表系列的气泡大小集合。"
type: docs
weight: 3500
url: /zh/cpp/aspose.words.drawing.charts/bubblesizecollection/
---
## BubbleSizeCollection class


表示图表系列的气泡大小集合。

```cpp
class BubbleSizeCollection : public System::Collections::Generic::IEnumerable<double>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Count](./get_count/)() | 获取此集合中的项目数量。 |
| [get_FormatCode](./get_formatcode/)() | 获取或设置应用于气泡大小的格式代码。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 获取或设置指定索引处的气泡大小值。 |
| [idx_set](./idx_set/)(int32_t, double) | 获取或设置指定索引处的气泡大小值。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | 用于 [Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode](./get_formatcode/) 的设置器。 |
| static [Type](./type/)() |  |
## 备注


该集合仅允许更改气泡大小。要向图表系列添加或插入新值，或删除值，可以使用 [ChartSeries](../chartseries/) 类的相应方法。

空的气泡大小值表示为 **NaN**。

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
