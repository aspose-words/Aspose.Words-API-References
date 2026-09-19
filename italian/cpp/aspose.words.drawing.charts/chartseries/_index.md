---
title: "Aspose::Words::Drawing::Charts::ChartSeries classe"
linktitle: "ChartSeries"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries classe. Rappresenta le proprietà della serie del grafico. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class


Rappresenta le proprietà della serie del grafico. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartSeries : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                    public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Aggiunge il valore X specificato alla serie del grafico. Se la serie supporta valori Y e dimensioni delle bolle, saranno vuoti per il valore X. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Aggiunge i valori X e Y specificati alla serie del grafico. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Aggiunge il valore X specificato, il valore Y e la dimensione della bolla alla serie del grafico. |
| [Clear](./clear/)() | Rimuove tutti i valori dei dati dalla serie del grafico. Il formato di tutti i punti dati individuali e delle etichette dei dati viene cancellato. |
| [ClearValues](./clearvalues/)() | Rimuove tutti i valori dei dati dalla serie del grafico preservando il formato dei punti dati e delle etichette dei dati. |
| [CopyFormatFrom](./copyformatfrom/)(int32_t) | Copia il formato predefinito del punto dati dal punto dati con l'indice specificato. |
| [get_Bubble3D](./get_bubble3d/)() override | Specifica se le bolle nel grafico a bolle devono avere un effetto 3-D applicato. |
| [get_BubbleSizes](./get_bubblesizes/)() | Ottiene una raccolta di dimensioni delle bolle per questa serie del grafico. |
| [get_DataLabels](./get_datalabels/)() | Specifica le impostazioni per le etichette dei dati dell'intera serie. |
| [get_DataPoints](./get_datapoints/)() const | Restituisce una raccolta di oggetti di formattazione per tutti i punti dati in questa serie. |
| [get_Explosion](./get_explosion/)() override | Specifica la quantità di spostamento del punto dati dal centro della torta. Può essere negativo; un valore negativo indica che la proprietà non è impostata e non deve essere applicata alcuna esplosione. Si applica solo ai grafici a torta. |
| [get_Format](./get_format/)() | Fornisce l'accesso alla formattazione di riempimento e linea della serie. |
| [get_HasDataLabels](./get_hasdatalabels/)() const | Ottiene o imposta un flag che indica se le etichette dei dati sono visualizzate per la serie. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Specifica se l'elemento genitore deve invertire i suoi colori se il valore è negativo. |
| [get_LegendEntry](./get_legendentry/)() | Ottiene una voce della legenda per questa serie di grafico. |
| [get_Marker](./get_marker/)() override | Specifica un marcatore dati. Il marcatore viene creato automaticamente quando richiesto. |
| [get_Name](./get_name/)() | Ottiene il nome della serie; se il nome non è impostato esplicitamente viene generato usando l'indice. Per impostazione predefinita restituisce Serie più indice basato su uno. |
| [get_SeriesType](./get_seriestype/)() | Ottiene il tipo di questa serie di grafico. |
| [get_Smooth](./get_smooth/)() const | Consente di specificare se la linea che collega i punti nel grafico deve essere smussata usando spline Catmull-Rom. |
| [get_XValues](./get_xvalues/)() | Ottiene una collezione di valori X per questa serie di grafico. |
| [get_YValues](./get_yvalues/)() | Ottiene una collezione di valori Y per questa serie di grafico. |
| [GetType](./gettype/)() const override |  |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Inserisce il valore X specificato nella serie di grafico all'indice specificato. Se la serie supporta valori Y e dimensioni delle bolle, questi saranno vuoti per il valore X. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Inserisce i valori X e Y specificati nella serie di grafico all'indice specificato. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Inserisce il valore X, il valore Y e la dimensione della bolla specificati nella serie di grafico all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Rimuove il valore X, il valore Y e la dimensione della bolla, se supportati, dalla serie di grafico all'indice specificato. Anche il punto dati corrispondente e l'etichetta dati vengono rimossi. |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Setter per [Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D](./get_bubble3d/). |
| [set_Explosion](./set_explosion/)(int32_t) override | Specifica la quantità di spostamento del punto dati dal centro della torta. Può essere negativo; un valore negativo indica che la proprietà non è impostata e non deve essere applicata alcuna esplosione. Si applica solo ai grafici a torta. |
| [set_HasDataLabels](./set_hasdatalabels/)(bool) | Setter per [Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels](./get_hasdatalabels/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Specifica se l'elemento genitore deve invertire i suoi colori se il valore è negativo. |
| [set_Name](./set_name/)(const System::String\&) | Imposta il nome della serie; se il nome non è impostato esplicitamente viene generato usando l'indice. Per impostazione predefinita restituisce Serie più indice basato su uno. |
| [set_Smooth](./set_smooth/)(bool) | Consente di specificare se la linea che collega i punti nel grafico deve essere smussata usando spline Catmull-Rom. |
| static [Type](./type/)() |  |
## Vedi anche

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
