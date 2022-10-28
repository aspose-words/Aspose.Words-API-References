---
title: InsertChart
second_title: Aspose.Words for C++ API Reference
description: Inserts an chart object into the document and scales it to the specified size.
type: docs
weight: 352
url: /cpp/aspose.words/documentbuilder/insertchart/
---
## DocumentBuilder.InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


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

You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples




Shows how to specify position and wrapping while inserting a chart. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->InsertChart(ChartType::Pie, RelativeHorizontalPosition::Margin, 100, RelativeVerticalPosition::Margin, 100, 200, 100, WrapType::Square);

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertedChartRelativePosition.docx");
```

## DocumentBuilder.InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double) method


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

You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples




Shows how to insert a pie chart into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Chart> chart = builder->InsertChart(ChartType::Pie, ConvertUtil::PixelToPoint(300), ConvertUtil::PixelToPoint(300))->get_Chart();
chart->get_Series()->Clear();
chart->get_Series()->Add(u"My fruit", MakeArray<String>({u"Apples", u"Bananas", u"Cherries"}), MakeArray<double>({1.3, 2.2, 1.5}));

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertPieChart.docx");
```

