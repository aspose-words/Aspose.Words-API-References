---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection class"
linktitle: "ChartDataLabelCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection classe. Rappresenta una raccolta di ChartDataLabel. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class


Rappresenta una raccolta di [ChartDataLabel](../chartdatalabel/). Per saperne di più, visita l'articolo della documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabelCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel>>,
                                 public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                                 public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormat](./clearformat/)() | Cancella il formato di tutti i [ChartDataLabel](../chartdatalabel/) in questa raccolta. |
| [get_Count](./get_count/)() | Restituisce il numero di [ChartDataLabel](../chartdatalabel/) in questa raccolta. |
| [get_Font](./get_font/)() | Fornisce l'accesso alla formattazione del carattere delle etichette dati dell'intera serie. |
| [get_Format](./get_format/)() | Fornisce l'accesso alla formattazione di riempimento e linea delle etichette dati. |
| [get_NumberFormat](./get_numberformat/)() | Ottiene un'istanza di [ChartNumberFormat](../chartnumberformat/) che consente di impostare il formato numerico per le etichette dati dell'intera serie. |
| [get_Orientation](./get_orientation/)() | Ottiene o imposta l'orientamento del testo delle etichette dati dell'intera serie. |
| [get_Position](./get_position/)() | Ottiene o imposta la posizione delle etichette dati. |
| [get_Rotation](./get_rotation/)() | Ottiene o imposta la rotazione delle etichette dati dell'intera serie in gradi. |
| [get_Separator](./get_separator/)() | Ottiene o imposta il separatore di stringa utilizzato per le etichette dati dell'intera serie. Il valore predefinito è una virgola, eccetto per i grafici a torta che mostrano solo il nome della categoria e la percentuale, dove viene usata una interruzione di riga. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Consente di specificare se visualizzare la dimensione della bolla per le etichette dati dell'intera serie. Si applica solo ai grafici a bolle. Il valore predefinito è **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Consente di specificare se visualizzare il nome della categoria per le etichette dati dell'intera serie. Il valore predefinito è **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Consente di specificare se visualizzare i valori dell'intervallo delle etichette dati nelle etichette dell'intera serie. Il valore predefinito è **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Consente di specificare se le linee guida delle etichette dati devono essere mostrate per le etichette dell'intera serie. Il valore predefinito è **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Consente di specificare se visualizzare la chiave della legenda per le etichette dati dell'intera serie. Il valore predefinito è **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Consente di specificare se visualizzare il valore percentuale per le etichette dati dell'intera serie. Il valore predefinito è **false**. Si applica solo ai grafici a torta. |
| [get_ShowSeriesName](./get_showseriesname/)() | Restituisce o imposta un Booleano per indicare il comportamento di visualizzazione del nome della serie per le etichette dati dell'intera serie. **true** per mostrare il nome della serie; **false** per nasconderlo. Per impostazione predefinita **false**. |
| [get_ShowValue](./get_showvalue/)() | Consente di specificare se visualizzare i valori nelle etichette dati dell'intera serie. Il valore predefinito è **false**. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce [ChartDataLabel](../chartdatalabel/) per l'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator](./get_separator/). |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName](./get_showcategoryname/). |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Consente di specificare se visualizzare i valori dell'intervallo delle etichette dati nelle etichette dell'intera serie. Il valore predefinito è **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines](./get_showleaderlines/). |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey](./get_showlegendkey/). |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage](./get_showpercentage/). |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName](./get_showseriesname/). |
| [set_ShowValue](./set_showvalue/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue](./get_showvalue/). |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
