---
title: "Aspose::Words::Drawing::Charts::ChartAxis class"
linktitle: "ChartAxis"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::ChartAxis 类。表示图表的轴选项。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class


表示图表的坐标轴选项。要了解更多，请访问[Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/)文档文章。

```cpp
class ChartAxis : public Aspose::Words::Drawing::Charts::Core::IDmlChartTitleHolder,
                  public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                  public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                  public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AxisBetweenCategories](./get_axisbetweencategories/)() | 获取或设置一个标志，指示值轴是否在类别之间跨越类别轴。 |
| [get_BaseTimeUnit](./get_basetimeunit/)() | 获取或设置在时间类别轴上表示的最小时间单位。 |
| [get_CategoryType](./get_categorytype/)() | 获取或设置类别轴的类型。 |
| [get_Crosses](./get_crosses/)() | 指定此轴如何跨越垂直轴。 |
| [get_CrossesAt](./get_crossesat/)() | 指定轴在垂直轴上的交叉位置。 |
| [get_DisplayUnit](./get_displayunit/)() | 指定值轴显示单位的缩放值。 |
| [get_Document](./get_document/)() | 返回包含父图表的文档。 |
| [get_Format](./get_format/)() | 提供对轴的线条格式和刻度标签填充的访问。 |
| [get_HasMajorGridlines](./get_hasmajorgridlines/)() | 获取或设置一个标志，指示轴是否具有主网格线。 |
| [get_HasMinorGridlines](./get_hasminorgridlines/)() | 获取或设置一个标志，指示轴是否具有次网格线。 |
| [get_Hidden](./get_hidden/)() | 获取或设置一个标志，指示此轴是否隐藏。 |
| [get_MajorTickMark](./get_majortickmark/)() | 获取或设置主刻度标记。 |
| [get_MajorUnit](./get_majorunit/)() | 获取或设置主刻度标记之间的距离。 |
| [get_MajorUnitIsAuto](./get_majorunitisauto/)() | 获取或设置一个标志，指示是否使用主刻度标记之间的默认距离。 |
| [get_MajorUnitScale](./get_majorunitscale/)() | 获取或设置时间类别轴上主刻度标记的比例值。 |
| [get_MinorTickMark](./get_minortickmark/)() | 获取或设置轴的次刻度标记。 |
| [get_MinorUnit](./get_minorunit/)() | 获取或设置次刻度标记之间的距离。 |
| [get_MinorUnitIsAuto](./get_minorunitisauto/)() | 获取或设置一个标志，指示是否使用次刻度标记之间的默认距离。 |
| [get_MinorUnitScale](./get_minorunitscale/)() | 获取或设置时间类别轴上次刻度标记的比例值。 |
| [get_NumberFormat](./get_numberformat/)() | 返回一个 [ChartNumberFormat](../chartnumberformat/) 对象，用于定义轴的数字格式。 |
| [get_ReverseOrder](./get_reverseorder/)() | 获取或设置一个标志，指示轴的值是否应以相反顺序显示，即从最大到最小。 |
| [get_Scaling](./get_scaling/)() | 提供对轴缩放选项的访问。 |
| [get_TickLabels](./get_ticklabels/)() | 提供对轴刻度标记标签属性的访问。 |
| [get_TickMarkSpacing](./get_tickmarkspacing/)() | 获取或设置绘制刻度标记的间隔。 |
| [get_Title](./get_title/)() | 提供对轴标题属性的访问。 |
| [get_Type](./get_type/)() const | 返回轴的类型。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisBetweenCategories](./set_axisbetweencategories/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories](./get_axisbetweencategories/)。 |
| [set_BaseTimeUnit](./set_basetimeunit/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_BaseTimeUnit](./get_basetimeunit/)。 |
| [set_CategoryType](./set_categorytype/)(Aspose::Words::Drawing::Charts::AxisCategoryType) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_CategoryType](./get_categorytype/)。 |
| [set_Crosses](./set_crosses/)(Aspose::Words::Drawing::Charts::AxisCrosses) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_Crosses](./get_crosses/)。 |
| [set_CrossesAt](./set_crossesat/)(double) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt](./get_crossesat/)。 |
| [set_HasMajorGridlines](./set_hasmajorgridlines/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines](./get_hasmajorgridlines/)。 |
| [set_HasMinorGridlines](./set_hasminorgridlines/)(bool) | 用于设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMinorGridlines](./get_hasminorgridlines/)。 |
| [set_Hidden](./set_hidden/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden](./get_hidden/)。 |
| [set_MajorTickMark](./set_majortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | 设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorTickMark](./get_majortickmark/)。 |
| [set_MajorUnit](./set_majorunit/)(double) | 设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnit](./get_majorunit/)。 |
| [set_MajorUnitIsAuto](./set_majorunitisauto/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitIsAuto](./get_majorunitisauto/)。 |
| [set_MajorUnitScale](./set_majorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | 设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale](./get_majorunitscale/)。 |
| [set_MinorTickMark](./set_minortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | 设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorTickMark](./get_minortickmark/)。 |
| [set_MinorUnit](./set_minorunit/)(double) | 设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnit](./get_minorunit/)。 |
| [set_MinorUnitIsAuto](./set_minorunitisauto/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto](./get_minorunitisauto/)。 |
| [set_MinorUnitScale](./set_minorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | 设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale](./get_minorunitscale/)。 |
| [set_ReverseOrder](./set_reverseorder/)(bool) | 设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_ReverseOrder](./get_reverseorder/)。 |
| [set_TickMarkSpacing](./set_tickmarkspacing/)(int32_t) | 设置 [Aspose::Words::Drawing::Charts::ChartAxis::get_TickMarkSpacing](./get_tickmarkspacing/)。 |
| static [Type](./type/)() |  |

## 示例



展示如何插入图表并修改其轴的外观。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 清除图表的演示数据系列，以便从空白图表开始。
chart->get_Series()->Clear();

// 为 X 轴插入带有类别的图表系列，并为 Y 轴提供相应的数值。
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// 图表轴具有多种可更改其外观的选项，
// 例如其方向、主/次单位刻度和刻度标记。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Category);
xAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

ASPOSE_ASSERT_EQ(doc, xAxis->get_Document());

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Automatic);
yAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
yAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::NextToAxis);
yAxis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
yAxis->get_TickLabels()->get_Font()->set_Color(System::Drawing::Color::get_Red());
yAxis->get_TickLabels()->set_Spacing(1);

// 柱形图没有 Z 轴。
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
