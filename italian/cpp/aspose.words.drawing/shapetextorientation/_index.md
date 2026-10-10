---
title: "Aspose::Words::Drawing::ShapeTextOrientation enum"
linktitle: "ShapeTextOrientation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeTextOrientation enum. Specifica l'orientamento del testo nelle forme in C++."
type: docs
weight: 37500
url: /it/cpp/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enum


Specifica l'orientamento del testo nelle forme.

```cpp
enum class ShapeTextOrientation
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Orizzontale | 0 | Il testo è disposto orizzontalmente (lr-tb). |
| Verso il basso | 1 | Il testo è ruotato di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl). |
| Verso l'alto | 2 | Il testo è ruotato di 90 gradi verso sinistra per apparire dal basso verso l'alto (bt-lr). |
| VerticalFarEast | 3 | I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl-v). |
| VerticalRotatedFarEast | 4 | I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso verticalmente, poi da sinistra a destra orizzontalmente (tb-lr-v). |
| WordArtVertical | 5 | Il testo è verticale, con una lettera sopra l'altra. |
| WordArtVerticalRightToLeft | 6 | Il testo è verticale, con una lettera sopra l'altra, poi da destra a sinistra orizzontalmente. |


## Esempi



Mostra come modificare l'orientamento e la rotazione per le etichette dati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// Mostra le etichette dati.
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// Definisci la forma dell'etichetta dati.
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// Imposta l'orientamento e la rotazione dell'etichetta dati per l'intera serie.
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// Modifica l'orientamento e la rotazione della prima etichetta dati.
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
