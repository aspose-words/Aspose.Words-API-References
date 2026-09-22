---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay yöntemi"
linktitle: "get_Overlay"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay yöntemi. Diğer grafik öğelerinin başlığın üzerine gelmesine izin verilip verilmeyeceğini belirler. Varsayılan değer C++'ta false'dur."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.drawing.charts/chartaxistitle/get_overlay/
---
## ChartAxisTitle::get_Overlay method


Diğer grafik öğelerinin başlığın üzerine gelmesine izin verilip verilmeyeceğini belirler. Varsayılan değer **false**dır.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay()
```


## Örnekler



Grafik eksen başlığının nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Varsayılan oluşturulan seriyi sil.
seriesColl->Clear();

seriesColl->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"}), System::MakeArray<double>({1, 2}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisXTitle = chart->get_AxisX()->get_Title();
chartAxisXTitle->set_Text(u"Categories");
chartAxisXTitle->set_Show(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisYTitle = chart->get_AxisY()->get_Title();
chartAxisYTitle->set_Text(u"Values");
chartAxisYTitle->set_Show(true);
chartAxisYTitle->set_Overlay(true);
chartAxisYTitle->get_Font()->set_Size(12);
chartAxisYTitle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.ChartAxisTitle.docx");
```

## Ayrıca Bakınız

* Class [ChartAxisTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
