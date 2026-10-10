---
title: "Aspose::Words::Drawing::PresetTexture Enum"
linktitle: "PresetTexture"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::PresetTexture Enum. Gibt die Textur an, die zum Füllen einer Form in C++ verwendet wird."
type: docs
weight: 32000
url: /de/cpp/aspose.words.drawing/presettexture/
---
## PresetTexture enum


Gibt die Textur an, die zum Füllen einer Form verwendet wird.

```cpp
enum class PresetTexture
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | -1 | Keine Textur. |
| BlueTissuePaper | 1 | Blaue Tissue-Papier-Textur. |
| Bouquet | 2 | Bouquet-Textur. |
| BrownMarble | 3 | Braune Marmor-Textur. |
| Leinwand | 4 | Leinwandtextur. |
| Kork | 5 | Korktextur. |
| Denim | 6 | Denimtextur. |
| Fischfossil | 7 | Fischfossiltextur. |
| Granit | 8 | Granittextur. |
| GrünerMarmor | 9 | Grüner Marmor Textur. |
| Mittelholz | 10 | Mittelholztextur. |
| Zeitungsdruck | 11 | Zeitungsdrucktextur. |
| Eiche | 12 | Eichentextur. |
| Papierbeutel | 13 | Papierbeuteltextur. |
| Papyrus | 14 | Papyrustextur. |
| Pergament | 15 | Pergamenttextur. |
| RosaPapiertuch | 16 | Rosa Tissuepapier-Textur. |
| LilaNetz | 17 | Lila-Netz-Textur. |
| RecyceltesPapier | 18 | Recycelte Papier-Textur. |
| Sand | 19 | Sand-Textur. |
| Bürobedarf | 20 | Bürobedarf-Textur. |
| Walnuss | 21 | Walnuss-Textur. |
| Wassertropfen | 22 | Wassertropfen-Textur. |
| WeißerMarmor | 23 | Weiße Marmor-Textur. |
| GewebteMatte | 24 | Gewebte Matten-Textur. |


## Beispiele



Zeige, wie man die Markerformatierung einstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Lösche standardmäßig generierte Serie.
chart->get_Series()->Clear();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<double>({0.7, 1.8, 2.6, 3.9}), System::MakeArray<double>({2.7, 3.2, 0.8, 1.7}));

// Markerformatierung festlegen.
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

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
