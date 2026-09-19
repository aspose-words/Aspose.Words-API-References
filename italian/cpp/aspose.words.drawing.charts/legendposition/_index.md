---
title: "Aspose::Words::Drawing::Charts::LegendPosition enum"
linktitle: "LegendPosition"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::LegendPosition enum. Specifica le possibili posizioni per una legenda del grafico in C++."
type: docs
weight: 29000
url: /it/cpp/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enum


Specifica le possibili posizioni per una legenda del grafico.

```cpp
enum class LegendPosition
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Nessuna legenda verrà mostrata per il grafico. |
| Inferiore | 1 | Specifica che la legenda deve essere disegnata nella parte inferiore del grafico. |
| Sinistra | 2 | Specifica che la legenda deve essere disegnata a sinistra del grafico. |
| Destra | 3 | Specifica che la legenda deve essere disegnata a destra del grafico. |
| Superiore | 4 | Specifica che la legenda deve essere disegnata nella parte superiore del grafico. |
| TopRight | 5 | Specifica che la legenda deve essere disegnata in alto a destra del grafico. |


## Esempi



Mostra come modificare l'aspetto della legenda di un grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Sposta la legenda del grafico nell'angolo in alto a destra.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Concedi più spazio ad altri elementi del grafico, come il grafico stesso, permettendo loro di sovrapporsi alla legenda.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
