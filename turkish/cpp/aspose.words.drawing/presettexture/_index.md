---
title: "Aspose::Words::Drawing::PresetTexture enum"
linktitle: "PresetTexture"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::PresetTexture enum. C++'ta bir şekli doldurmak için kullanılacak dokuyu belirtir."
type: docs
weight: 32000
url: /tr/cpp/aspose.words.drawing/presettexture/
---
## PresetTexture enum


Bir şekli doldurmak için kullanılacak dokuyu belirtir.

```cpp
enum class PresetTexture
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | -1 | Doku Yok. |
| BlueTissuePaper | 1 | Mavi kağıt havlu dokusu. |
| Bouquet | 2 | Buket dokusu. |
| Kahverengi Mermer | 3 | Kahverengi mermer dokusu. |
| Tuval | 4 | Tuval dokusu. |
| Mantar | 5 | Mantar dokusu. |
| Kot | 6 | Kot dokusu. |
| Balık Fosili | 7 | Balık fosili dokusu. |
| Granit | 8 | Granit dokusu. |
| Yeşil Mermer | 9 | Yeşil mermer dokusu. |
| Orta Ahşap | 10 | Orta ahşap dokusu. |
| Gazete Kağıdı | 11 | Gazete kağıdı dokusu. |
| Meşe | 12 | Meşe dokusu. |
| Kağıt Torba | 13 | Kağıt torba dokusu. |
| Papirüs | 14 | Papirüs dokusu. |
| Parşömen | 15 | Parşömen dokusu. |
| PembeKağıt | 16 | Pembe kağıt dokusu. |
| MorAğ | 17 | Mor ağ dokusu. |
| GeriDönüştürülmüşKağıt | 18 | Geri dönüştürülmüş kağıt dokusu. |
| Kum | 19 | Kum dokusu. |
| Kırtasiye | 20 | Kırtasiye dokusu. |
| Ceviz | 21 | Ceviz dokusu. |
| SuDamlası | 22 | Su damlaları dokusu. |
| BeyazMermer | 23 | Beyaz mermer dokusu. |
| DokumaMat | 24 | Dokuma mat dokusu. |


## Örnekler



İşaretleyici biçimlendirmesinin nasıl ayarlanacağını göster.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Varsayılan oluşturulan seriyi sil.
chart->get_Series()->Clear();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<double>({0.7, 1.8, 2.6, 3.9}), System::MakeArray<double>({2.7, 3.2, 0.8, 1.7}));

// İşaretleyici biçimlendirmesini ayarla.
series->get_Marker()->set_Size(40);
series->get_Marker()->set_Symbol(Aspose::Words::Drawing::Charts::MarkerSymbol::Square);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Denim);
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Stroke()->set_BackColor(System::Drawing::Color::get_Red());
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::WaterDroplets);
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Stroke()->set_Visible(false);
dataPoints->idx_get(2)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::GreenMarble);
dataPoints->idx_get(2)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Oak);
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Stroke()->set_Transparency(0.5);

doc->Save(get_ArtifactsDir() + u"Charts.MarkerFormatting.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
