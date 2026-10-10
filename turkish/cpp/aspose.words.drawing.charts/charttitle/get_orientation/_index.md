---
title: "Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation yöntemi"
linktitle: "get_Orientation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation yöntemi. Grafik başlığı metninin yönelimini alır veya ayarlar C++'da."
type: docs
weight: 1875
url: /tr/cpp/aspose.words.drawing.charts/charttitle/get_orientation/
---
## ChartTitle::get_Orientation method


Grafik başlığı metninin yönünü alır veya ayarlar.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation()
```


## Örnekler



Grafik ve eksen başlıklarının yönelim ve dönüşünün nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

chart->get_Title()->set_Text(u"Sample Chart");
chart->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_Title()->set_Rotation(90);

// Başlık özelliklerini ayarlamadan önce, bu başlığın görüntüleneceğinden emin olun.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->set_Text(u"X Axis");
chart->get_AxisX()->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_AxisX()->get_Title()->set_Rotation(-90);

doc->Save(get_ArtifactsDir() + u"Charts.TitleOrientation.docx");
```

## Ayrıca Bakınız

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
