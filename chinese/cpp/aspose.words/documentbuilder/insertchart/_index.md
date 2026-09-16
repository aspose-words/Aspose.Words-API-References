---
title: "Aspose::Words::DocumentBuilder::InsertChart 方法"
linktitle: "InsertChart"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertChart 方法。在 C++ 中向文档插入图表对象并将其缩放到指定大小。"
type: docs
weight: 30000
url: /zh/cpp/aspose.words/documentbuilder/insertchart/
---
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


在文档中插入图表对象并将其缩放到指定大小。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | 要插入到文档中的图表类型。 |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | 指定测量图像距离的起点位置。 |
| left | double | 从原点到图像左侧的距离（点）。 |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | 指定测量图像距离的起点位置。 |
| top | double | 从原点到图像顶部的距离（点）。 |
| width | double | 图像的宽度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| height | double | 图像的高度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| wrapType | Aspose::Words::Drawing::WrapType | 指定文本环绕图像的方式。 |

### ReturnValue

刚刚插入的图像节点。
## 备注


您可以使用此方法返回的 [Shape](../../../aspose.words.drawing/shape/) 对象更改图像大小、位置、定位方式以及其他设置。

## 示例



展示如何在插入图表时指定位置和环绕方式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100, 200, 100, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertedChartRelativePosition.docx");
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) method


在文档中插入图表对象并将其缩放到指定大小。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | 要插入到文档中的图表类型。 |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | 指定测量图像距离的起点位置。 |
| left | double | 从原点到图像左侧的距离（点）。 |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | 指定测量图像距离的起点位置。 |
| top | double | 从原点到图像顶部的距离（点）。 |
| width | double | 图像的宽度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| height | double | 图像的高度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| wrapType | Aspose::Words::Drawing::WrapType | 指定文本环绕图像的方式。 |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | 插入图表的样式。 |

### ReturnValue

刚刚插入的图像节点。
## 备注


您可以使用此方法返回的 [Shape](../../../aspose.words.drawing/shape/) 对象更改图像大小、位置、定位方式以及其他设置。

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double) method


在文档中插入图表对象并将其缩放到指定大小。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | 要插入到文档中的图表类型。 |
| width | double | 图像的宽度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| height | double | 图像的高度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |

### ReturnValue

刚刚插入的图像节点。
## 备注


您可以使用此方法返回的 [Shape](../../../aspose.words.drawing/shape/) 对象更改图像大小、位置、定位方式以及其他设置。

## 示例



展示如何在文档中插入饼图。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::ConvertUtil::PixelToPoint(300), Aspose::Words::ConvertUtil::PixelToPoint(300))->get_Chart();
chart->get_Series()->Clear();
chart->get_Series()->Add(u"My fruit", System::MakeArray<System::String>({u"Apples", u"Bananas", u"Cherries"}), System::MakeArray<double>({1.3, 2.2, 1.5}));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertPieChart.docx");
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) method


在文档中插入图表对象并将其缩放到指定大小。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | 要插入到文档中的图表类型。 |
| width | double | 图像的宽度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| height | double | 图像的高度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | 插入图表的样式。 |

### ReturnValue

刚刚插入的图像节点。
## 备注


您可以使用此方法返回的 [Shape](../../../aspose.words.drawing/shape/) 对象更改图像大小、位置、定位方式以及其他设置。

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
