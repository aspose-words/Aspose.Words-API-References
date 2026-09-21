---
title: "Aspose::Words::Drawing::ShapeTextOrientation enum"
linktitle: "ShapeTextOrientation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeTextOrientation enum. Anger orienteringen av text i former i C++."
type: docs
weight: 37500
url: /sv/cpp/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enum


Anger orienteringen av text i former.

```cpp
enum class ShapeTextOrientation
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Horisontell | 0 | Texten är ordnad horisontellt (lr-tb). |
| Nedåt | 1 | Texten roteras 90 grader åt höger för att visas från topp till botten (tb-rl). |
| Uppåt | 2 | Texten roteras 90 grader åt vänster för att visas från botten till toppen (bt-lr). |
| VerticalFarEast | 3 | Far East-tecken visas vertikalt, annan text roteras 90 grader åt höger för att visas från topp till botten (tb-rl-v). |
| VerticalRotatedFarEast | 4 | Far East-tecken visas vertikalt, annan text roteras 90 grader åt höger för att visas från topp till botten vertikalt, sedan från vänster till höger horisontellt (tb-lr-v). |
| WordArtVertical | 5 | Texten är vertikal, med en bokstav ovanpå den andra. |
| WordArtVerticalRightToLeft | 6 | Texten är vertikal, med en bokstav ovanpå den andra, sedan från höger till vänster horisontellt. |


## Exempel



Visar hur man ändrar orientering och rotation för datamärkningar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// Visa datamärkningar.
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// Definiera datamärkningsform.
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// Ställ in datamärkningens orientering och rotation för hela serien.
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// Ändra orientering och rotation för den första datamärkningen.
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
