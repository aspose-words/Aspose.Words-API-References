---
title: "Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType yöntemi"
linktitle: "get_ShapeType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType yöntemi. C++'ta üst grafik öğesinin şekil tipini alır veya ayarlar."
type: docs
weight: 2500
url: /tr/cpp/aspose.words.drawing.charts/chartformat/get_shapetype/
---
## ChartFormat::get_ShapeType method


Üst grafik öğesinin şekil tipini alır veya ayarlar.

```cpp
Aspose::Words::Drawing::Charts::ChartShapeType Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType()
```


## Örnekler



Grafik veri etiketleri için doldurma, kenarlık ve çağrı biçimlendirmesinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Varsayılan oluşturulan seriyi sil.
chart->get_Series()->Clear();

// Yeni seri ekle.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2", u"AW Category 3", u"AW Category 4"}), System::MakeArray<double>({100, 200, 300, 400}));

// Veri etiketlerini göster.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);

// Veri etiketlerini çağrı olarak biçimlendir.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> format = series->get_DataLabels()->get_Format();
format->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::WedgeRectCallout);
format->get_Stroke()->set_Color(System::Drawing::Color::get_DarkGreen());
format->get_Fill()->Solid(System::Drawing::Color::get_Green());
series->get_DataLabels()->get_Font()->set_Color(System::Drawing::Color::get_Yellow());

// Tek bir veri etiketinin doldurma ve kenarlığını değiştir.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> labelFormat = series->get_DataLabels()->idx_get(0)->get_Format();
labelFormat->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());
labelFormat->get_Fill()->Solid(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.FormatDataLables.docx");
```

## Ayrıca Bakınız

* Enum [ChartShapeType](../../chartshapetype/)
* Class [ChartFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
