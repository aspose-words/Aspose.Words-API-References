---
title: "Aspose::Words::Drawing::ShapeTextOrientation enum"
linktitle: "ShapeTextOrientation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeTextOrientation enum. Şekillerdeki metnin yönünü C++'da belirtir."
type: docs
weight: 37500
url: /tr/cpp/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enum


Şekillerdeki metnin yönünü belirtir.

```cpp
enum class ShapeTextOrientation
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Yatay | 0 | Metin yatay olarak düzenlenir (lr-tb). |
| Aşağı | 1 | Metin, üstten alta görünmesi için sağa doğru 90 derece döndürülür (tb-rl). |
| Yukarı | 2 | Metin, alttan üste görünmesi için sola doğru 90 derece döndürülür (bt-lr). |
| VerticalFarEast | 3 | Uzak Doğu karakterleri dikey olarak görünür, diğer metin sağa doğru 90 derece döndürülerek üstten alta (tb-rl-v) görünür. |
| VerticalRotatedFarEast | 4 | Uzak Doğu karakterleri dikey olarak görünür, diğer metin sağa doğru 90 derece döndürülerek önce üstten alta dikey, ardından soldan sağa yatay (tb-lr-v) görünür. |
| WordArtVertical | 5 | Metin dikeydir, bir harf diğerinin üstünde. |
| WordArtVerticalRightToLeft | 6 | Metin dikeydir, bir harf diğerinin üstünde, ardından yatay olarak sağdan sola. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
