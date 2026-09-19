---
title: "classe Aspose::Words::Drawing::Charts::ChartSeriesGroup"
linktitle: "ChartSeriesGroup"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Drawing::Charts::ChartSeriesGroup. Rappresenta le proprietà di un gruppo di serie del grafico, cioè le proprietà delle serie del grafico dello stesso tipo associate agli stessi assi in C++."
type: docs
weight: 17334
url: /it/cpp/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class


Rappresenta le proprietà di un gruppo di serie del grafico, cioè le proprietà delle serie del grafico dello stesso tipo associate agli stessi assi.

```cpp
class ChartSeriesGroup : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AxisGroup](./get_axisgroup/)() | Ottiene o imposta il gruppo di assi a cui appartiene questo gruppo di serie. |
| [get_AxisX](./get_axisx/)() | Fornisce l'accesso alle proprietà dell'asse X di questo gruppo di serie. |
| [get_AxisY](./get_axisy/)() | Fornisce l'accesso alle proprietà dell'asse Y di questo gruppo di serie. |
| [get_BubbleScale](./get_bubblescale/)() | Ottiene o imposta la dimensione delle bolle come percentuale della loro dimensione predefinita. |
| [get_DoughnutHoleSize](./get_doughnutholesize/)() | Ottiene o imposta la dimensione del foro del grafico a ciambella principale come percentuale. |
| [get_FirstSliceAngle](./get_firstsliceangle/)() | Ottiene o imposta l'angolo, in gradi, della prima fetta del grafico a torta principale. |
| [get_GapWidth](./get_gapwidth/)() | Ottiene o imposta la percentuale della larghezza dello spazio tra gli elementi del grafico. |
| [get_Overlap](./get_overlap/)() | Ottiene o imposta la percentuale di quanto le barre o le colonne della serie si sovrappongono. |
| [get_SecondSectionSize](./get_secondsectionsize/)() | Ottiene o imposta la dimensione della sezione secondaria del grafico a torta come percentuale. |
| [get_Series](./get_series/)() | Ottiene una raccolta di serie che appartengono a questo gruppo di serie. |
| [get_SeriesType](./get_seriestype/)() | Ottiene il tipo di serie di grafico incluso in questo gruppo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisGroup](./set_axisgroup/)(Aspose::Words::Drawing::Charts::AxisGroup) | Impostatore per [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup](./get_axisgroup/). |
| [set_BubbleScale](./set_bubblescale/)(int32_t) | Impostatore per [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale](./get_bubblescale/). |
| [set_DoughnutHoleSize](./set_doughnutholesize/)(int32_t) | Impostatore per [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize](./get_doughnutholesize/). |
| [set_FirstSliceAngle](./set_firstsliceangle/)(int32_t) | Impostatore per [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle](./get_firstsliceangle/). |
| [set_GapWidth](./set_gapwidth/)(int32_t) | Impostatore per [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth](./get_gapwidth/). |
| [set_Overlap](./set_overlap/)(int32_t) | Impostatore per [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap](./get_overlap/). |
| [set_SecondSectionSize](./set_secondsectionsize/)(int32_t) | Impostatore per [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize](./get_secondsectionsize/). |
| static [Type](./type/)() |  |
## Note


I grafici combinati contengono più gruppi di serie di grafico, con un gruppo separato per ogni tipo di serie.

Inoltre, è possibile creare un gruppo di serie di grafico per assegnare assi secondari a una o più serie di grafico.

Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

## Esempi



Mostra come lavorare con l'asse secondario del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Elimina la serie generata di default.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Crea un gruppo di serie aggiuntivo, anch'esso di tipo linea.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Specifica l'uso degli assi secondari per il nuovo gruppo di serie.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// Nascondi l'asse X secondario.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// Definisci il titolo dell'asse Y secondario.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Aggiungi una serie al nuovo gruppo di serie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
