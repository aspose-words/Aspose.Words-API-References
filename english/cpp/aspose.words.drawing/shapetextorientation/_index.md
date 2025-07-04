---
title: Aspose::Words::Drawing::ShapeTextOrientation enum
linktitle: ShapeTextOrientation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeTextOrientation enum. Specifies orientation of text in shapes in C++.'
type: docs
weight: 37500
url: /cpp/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enum


Specifies orientation of text in shapes.

```cpp
enum class ShapeTextOrientation
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Horizontal | 0 | Text is arranged horizontally (lr-tb). |
| Downward | 1 | Text is rotated 90 degrees to the right to appear from top to bottom (tb-rl). |
| Upward | 2 | Text is rotated 90 degrees to the left to appear from bottom to top (bt-lr). |
| VerticalFarEast | 3 | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom (tb-rl-v). |
| VerticalRotatedFarEast | 4 | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom vertically, then left to right horizontally (tb-lr-v). |
| WordArtVertical | 5 | Text is vertical, with one letter on top of the other. |
| WordArtVerticalRightToLeft | 6 | Text is vertical, with one letter on top of the other, then right to left horizontally. |


## Examples



Shows how to change orientation and rotation for data labels. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// Show data labels.
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// Define data label shape.
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// Set data label orientation and rotation for the entire series.
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// Change orientation and rotation of the first data label.
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
