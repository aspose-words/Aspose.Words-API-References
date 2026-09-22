---
title: "Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation metodu"
linktitle: "get_Orientation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation metodu. C++'ta işaret etiketi metninin yönünü alır veya ayarlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.drawing.charts/axisticklabels/get_orientation/
---
## AxisTickLabels::get_Orientation method


İşaretleme etiketi metninin yönünü alır veya ayarlar.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation()
```

## Açıklamalar


Varsayılan değer [Horizontal](../../../aspose.words.drawing/shapetextorientation/)dır.

Bazı [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/) değerlerinin değer eksenlerindeki işaret etiketi metni yönünü etkilemediğini unutmayın.

## Örnekler



Eksen işaret etiketlerinin yönelim ve dönüşünü nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir sütun grafik ekleyin.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> xTickLabels = shape->get_Chart()->get_AxisX()->get_TickLabels();
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> yTickLabels = shape->get_Chart()->get_AxisY()->get_TickLabels();

// Eksen işaret etiketlerinin yönelim ve dönüşünü ayarlayın.
xTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
xTickLabels->set_Rotation(-30);
yTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
yTickLabels->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.TickLabelsOrientationRotation.docx");
```

## Ayrıca Bakınız

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [AxisTickLabels](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
