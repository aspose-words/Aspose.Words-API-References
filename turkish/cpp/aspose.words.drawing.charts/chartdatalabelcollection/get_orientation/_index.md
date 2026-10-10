---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation metodu"
linktitle: "get_Orientation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation metodu. C++'da tüm serinin veri etiketlerinin metin yönelimini alır veya ayarlar."
type: docs
weight: 5334
url: /tr/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_orientation/
---
## ChartDataLabelCollection::get_Orientation method


Tüm serinin veri etiketlerinin metin yönelimini alır veya ayarlar.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation()
```


## Örnekler



Veri etiketleri için yön ve dönüşün nasıl değiştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// Veri etiketlerini göster.
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// Veri etiketi şekli tanımla.
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// Tüm seri için veri etiketi yönünü ve dönüşünü ayarla.
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// İlk veri etiketinin yönünü ve dönüşünü değiştir.
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## Ayrıca Bakınız

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
