---
title: "Aspose::Words::Drawing::Charts::ChartFormat classe"
linktitle: "ChartFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartFormat classe. Rappresenta la formattazione di un elemento del grafico. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class


Rappresenta la formattazione di un elemento del grafico. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartFormat : public Aspose::Words::Drawing::Core::IFillable,
                    public Aspose::Words::Drawing::Core::IStrokable
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Fill](./get_fill/)() | Ottiene la formattazione del riempimento per l'elemento grafico genitore. |
| [get_IsDefined](./get_isdefined/)() | Ottiene un flag che indica se è definita qualche formattazione. |
| [get_ShapeType](./get_shapetype/)() | Ottiene o imposta il tipo di forma dell'elemento grafico genitore. |
| [get_Stroke](./get_stroke/)() | Ottiene la formattazione della linea per l'elemento grafico genitore. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ShapeType](./set_shapetype/)(Aspose::Words::Drawing::Charts::ChartShapeType) | Setter per [Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType](./get_shapetype/). |
| [SetDefaultFill](./setdefaultfill/)() | Reimposta il riempimento dell'elemento grafico al valore predefinito. |
| static [Type](./type/)() |  |

## Esempi



Mostra come utilizzare la formattazione del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Elimina le serie generate per impostazione predefinita.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});
series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));

// Formatta lo sfondo del grafico.
chart->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_DarkSlateGray());

// Nascondi le etichette dei tick dell'asse.
chart->get_AxisX()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);
chart->get_AxisY()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);

// Formatta il titolo del grafico.
chart->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Formatta il titolo dell'asse.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Formatta la legenda.
chart->get_Legend()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

doc->Save(get_ArtifactsDir() + u"Charts.ChartFormat.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
