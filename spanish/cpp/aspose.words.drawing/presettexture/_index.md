---
title: "Aspose::Words::Drawing::PresetTexture enumeración"
linktitle: "PresetTexture"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::PresetTexture enumeración. Especifica la textura que se utilizará para rellenar una forma en C++."
type: docs
weight: 32000
url: /es/cpp/aspose.words.drawing/presettexture/
---
## PresetTexture enum


Especifica la textura que se usará para rellenar una forma.

```cpp
enum class PresetTexture
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | -1 | Sin textura. |
| BlueTissuePaper | 1 | Textura de papel de seda azul. |
| Bouquet | 2 | Textura de ramo. |
| BrownMarble | 3 | Textura de mármol marrón. |
| Canvas | 4 | Textura de lienzo. |
| Cork | 5 | Textura de corcho. |
| Denim | 6 | Textura de denim. |
| FishFossil | 7 | Textura de fósil de pez. |
| Granite | 8 | Textura de granito. |
| GreenMarble | 9 | Textura de mármol verde. |
| MediumWood | 10 | Textura de madera mediana. |
| Newsprint | 11 | Textura de papel periódico. |
| Oak | 12 | Textura de roble. |
| PaperBag | 13 | Textura de bolsa de papel. |
| Papyrus | 14 | Textura de papiro. |
| Parchment | 15 | Textura de pergamino. |
| PinkTissuePaper | 16 | Textura de papel tisú rosa. |
| PurpleMesh | 17 | Textura de malla púrpura. |
| RecycledPaper | 18 | Textura de papel reciclado. |
| Sand | 19 | Textura de arena. |
| Stationery | 20 | Textura de papelería. |
| Walnut | 21 | Textura de nogal. |
| WaterDroplets | 22 | Textura de gotas de agua. |
| WhiteMarble | 23 | Textura de mármol blanco. |
| WovenMat | 24 | Textura de alfombra tejida. |


## Ejemplos



Muestra cómo establecer el formato del marcador.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Eliminar la serie generada por defecto.
chart->get_Series()->Clear();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<double>({0.7, 1.8, 2.6, 3.9}), System::MakeArray<double>({2.7, 3.2, 0.8, 1.7}));

// Establecer el formato del marcador.
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

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
