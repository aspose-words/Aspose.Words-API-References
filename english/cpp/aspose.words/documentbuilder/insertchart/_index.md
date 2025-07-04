---
title: Aspose::Words::DocumentBuilder::InsertChart method
linktitle: InsertChart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertChart method. Inserts an chart object into the document and scales it to the specified size in C++.'
type: docs
weight: 30000
url: /cpp/aspose.words/documentbuilder/insertchart/
---
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserts an chart object into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | The chart type to insert into the document. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | double | Distance in points from the origin to the left side of the image. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | double | Distance in points from the origin to the top side of the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifies how to wrap text around the image. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to specify position and wrapping while inserting a chart. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100, 200, 100, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertedChartRelativePosition.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) method


Inserts an chart object into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parameter | Type | Description |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | The chart type to insert into the document. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifies where the distance to the image is measured from. |
| left | double | Distance in points from the origin to the left side of the image. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifies where the distance to the image measured from. |
| top | double | Distance in points from the origin to the top side of the image. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifies how to wrap text around the image. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | The style of the inserted chart. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## See Also

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


Inserts an chart object into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height)
```


| Parameter | Type | Description |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | The chart type to insert into the document. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert a pie chart into a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::ConvertUtil::PixelToPoint(300), Aspose::Words::ConvertUtil::PixelToPoint(300))->get_Chart();
chart->get_Series()->Clear();
chart->get_Series()->Add(u"My fruit", System::MakeArray<System::String>({u"Apples", u"Bananas", u"Cherries"}), System::MakeArray<double>({1.3, 2.2, 1.5}));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertPieChart.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) method


Inserts an chart object into the document and scales it to the specified size.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parameter | Type | Description |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | The chart type to insert into the document. |
| width | double | The width of the image in points. Can be a negative or zero value to request 100% scale. |
| height | double | The height of the image in points. Can be a negative or zero value to request 100% scale. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | The style of the inserted chart. |

### ReturnValue

The image node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
