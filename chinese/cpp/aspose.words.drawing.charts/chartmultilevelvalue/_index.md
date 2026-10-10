---
title: "Aspose::Words::Drawing::Charts::ChartMultilevelValue class"
linktitle: "ChartMultilevelValue"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartMultilevelValue class. 表示用于在 C++ 中显示多层数据的图表值。"
type: docs
weight: 14500
url: /zh/cpp/aspose.words.drawing.charts/chartmultilevelvalue/
---
## ChartMultilevelValue class


表示用于显示多层次数据的图表值。

```cpp
class ChartMultilevelValue : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&, const System::String\&, const System::String\&) | 初始化此类的一个新实例，该实例表示三层值。 |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&, const System::String\&) | 初始化此类的一个新实例，该实例表示两层值。 |
| [ChartMultilevelValue](./chartmultilevelvalue/)(const System::String\&) | 初始化此类的一个新实例，该实例表示单层值。 |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | 获取一个标志，指示指定的对象是否等于当前的多层数据对象。 |
| [get_Level1](./get_level1/)() const | 获取此值所指的图表顶层名称。 |
| [get_Level2](./get_level2/)() const | 获取此值所指的图表中间层名称。 |
| [get_Level3](./get_level3/)() const | 获取此值所指的图表底层名称。 |
| [GetHashCode](./gethashcode/)() const override | 获取当前多层数据对象的哈希码。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## 示例



展示如何创建树状图表。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个树状图表。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Treemap, 450, 280);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"World Population");

// 删除默认生成的系列。
chart->get_Series()->Clear();

// 添加一个系列。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Population by Region", System::MakeArray<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartMultilevelValue>>({System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"China"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"India"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Indonesia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Pakistan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Bangladesh"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Japan"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Philippines"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Asia", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Nigeria"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Ethiopia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Egypt"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Africa", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Russia"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Germany"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Europe", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Brazil"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Mexico"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Latin America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"United States", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Northern America", u"Other"), System::MakeObject<Aspose::Words::Drawing::Charts::ChartMultilevelValue>(u"Oceania")}), System::MakeArray<double>({1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000, 223800000, 107334000, 105914499, 903000000, 146150789, 84607016, 516000000, 203080756, 129713690, 310000000, 335893238, 35000000, 42000000}));

// 显示数据标签。
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowCategoryName(true);
System::String thousandSeparator = System::Globalization::CultureInfo::get_CurrentCulture()->get_NumberFormat()->get_CurrencyGroupSeparator();
series->get_DataLabels()->get_NumberFormat()->set_FormatCode(System::String::Format(u"#{0}0", thousandSeparator));

doc->Save(get_ArtifactsDir() + u"Charts.Treemap.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
