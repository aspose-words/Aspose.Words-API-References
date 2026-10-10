---
title: "Aspose::Words::Drawing::Charts::ChartLegend class"
linktitle: "ChartLegend"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartLegend class. Rappresenta le proprietà della legenda del grafico. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class


Rappresenta le proprietà della legenda del grafico. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegend : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                    public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Font](./get_font/)() | Fornisce l'accesso alla formattazione del carattere predefinita delle voci della legenda. Per sovrascrivere la formattazione del carattere per una voce specifica della legenda, usa il[Font](../chartlegendentry/get_font/) proprietà. |
| [get_Format](./get_format/)() | Fornisce l'accesso alla formattazione di riempimento e linea della legenda. |
| [get_LegendEntries](./get_legendentries/)() const | Restituisce una raccolta di voci della legenda per tutte le serie e le linee di tendenza del grafico principale. |
| [get_Overlay](./get_overlay/)() const | Determina se altri elementi del grafico devono poter sovrapporsi alla legenda. Il valore predefinito è **false**. |
| [get_Position](./get_position/)() | Specifica la posizione della legenda su un grafico. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Overlay](./set_overlay/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay](./get_overlay/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::LegendPosition) | Impostatore per [Aspose::Words::Drawing::Charts::ChartLegend::get_Position](./get_position/). |
| static [Type](./type/)() |  |

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
