---
title: "Enum Aspose::Words::Drawing::Charts::ChartStyle"
linktitle: "ChartStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartStyle enum. Specifica gli stili predefiniti di un grafico in C++."
type: docs
weight: 27875
url: /it/cpp/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enum


Specifica gli stili predefiniti di un grafico.

```cpp
enum class ChartStyle
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Normale | 0 | Rappresenta lo stile predefinito del grafico. |
| Muted | 1 | Uno stile con colori smorzati. |
| Saturated | 2 | Uno stile con colori più saturi. |
| Shaded | 3 | Uno stile con punti dati ombreggiati. |
| Flat | 4 | Uno stile con punti dati piatti senza gradiente. |
| Shadowed | 5 | Uno stile con punti dati che hanno un'ombra. |
| Gradiente | 6 | Uno stile con riempimento a gradiente dei punti dati. |
| Originale | 7 | Uno stile con un aspetto originale del grafico. |
| Transparent1 | 8 | Uno stile con punti dati trasparenti. |
| Transparent2 | 9 | Uno stile con punti dati trasparenti. |
| Contorno | 10 | Uno stile con punti dati senza riempimento, ma solo con un contorno. |
| OutlineBlack | 11 | Uno stile con sfondo del grafico nero, in cui i punti dati non hanno riempimento, ma solo un contorno. |
| Nero | 12 | Uno stile con sfondo del grafico nero. |
| Grey | 13 | Uno stile con sfondo del grafico a gradiente grigio. |
| Blu | 14 | Uno stile con sfondo del grafico blu. |
| ShadedPlot | 15 | Uno stile, in cui l'area del grafico è ombreggiata. |


## Esempi



Mostra come impostare e ottenere lo stile del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un grafico nello stile Nero.
builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 250, Aspose::Words::Drawing::Charts::ChartStyle::Black);

doc->Save(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

// Ottieni un grafico da aggiornare.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Ottieni lo stile del grafico.
ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartStyle::Black, chart->get_Style());
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
