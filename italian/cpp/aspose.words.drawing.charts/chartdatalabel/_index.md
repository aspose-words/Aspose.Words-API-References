---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel class"
linktitle: "ChartDataLabel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel class. Rappresenta l'etichetta dati su un punto del grafico o su una linea di tendenza. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class


Rappresenta l'etichetta dati su un punto o una linea di tendenza del grafico. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabel : public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                       public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormat](./clearformat/)() | Cancella il formato di questa etichetta dati. Le proprietà sono impostate ai valori predefiniti definiti nella raccolta di etichette dati padre. |
| [get_Font](./get_font/)() | Fornisce l'accesso alla formattazione del carattere di questa etichetta dati. |
| [get_Format](./get_format/)() | Fornisce l'accesso alla formattazione di riempimento e linea dell'etichetta dati. |
| [get_Index](./get_index/)() | Specifica l'indice dell'elemento contenitore. Questo indice determinerà a quale collezione di figli del genitore si applica l'elemento. Il valore predefinito è 0. |
| [get_IsHidden](./get_ishidden/)() | Ottiene/imposta un flag che indica se questa etichetta è nascosta. Il valore predefinito è **false**. |
| [get_IsVisible](./get_isvisible/)() | Restituisce **true** se questa etichetta dati ha qualcosa da visualizzare. |
| [get_Left](./get_left/)() | Ottiene o imposta la distanza dell'etichetta dati in punti dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [Position](./get_position/), a seconda del valore della proprietà [LeftMode](./get_leftmode/). |
| [get_LeftMode](./get_leftmode/)() | Ottiene o imposta la modalità di interpretazione del valore della proprietà [Left](./get_left/): se imposta la posizione dell'etichetta dati dal bordo sinistro del grafico o dalla posizione specificata dalla sua proprietà [Position](./get_position/). |
| [get_NumberFormat](./get_numberformat/)() | Restituisce il formato numerico dell'elemento padre. |
| [get_Orientation](./get_orientation/)() | Ottiene o imposta l'orientamento del testo dell'etichetta. |
| [get_Position](./get_position/)() | Ottiene o imposta la posizione dell'etichetta dati. |
| [get_Rotation](./get_rotation/)() | Ottiene o imposta la rotazione dell'etichetta in gradi. |
| [get_Separator](./get_separator/)() | Ottiene il separatore di stringa usato per le etichette dati su un grafico. Il valore predefinito è una virgola, eccetto per i grafici a torta che mostrano solo il nome della categoria e la percentuale, dove viene utilizzato un ritorno a capo. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Consente di specificare se la dimensione della bolla deve essere visualizzata per le etichette dati su un grafico. Si applica solo ai grafici a bolle. Il valore predefinito è **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Consente di specificare se il nome della categoria deve essere visualizzato per le etichette dei dati in un grafico. Il valore predefinito è **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Consente di specificare se i valori dell'intervallo delle etichette dei dati devono essere visualizzati nelle etichette dei dati. Il valore predefinito è **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Consente di specificare se le linee guida delle etichette dei dati devono essere mostrate. Il valore predefinito è **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Consente di specificare se la chiave della legenda deve essere visualizzata per le etichette dei dati in un grafico. Il valore predefinito è **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Consente di specificare se il valore percentuale deve essere visualizzato per le etichette dei dati in un grafico. Il valore predefinito è **false**. |
| [get_ShowSeriesName](./get_showseriesname/)() | Restituisce un Boolean per indicare il comportamento di visualizzazione del nome della serie per le etichette dei dati in un grafico. **true** per mostrare il nome della serie; **false** per nasconderlo. Per impostazione predefinita **false**. |
| [get_ShowValue](./get_showvalue/)() | Consente di specificare se i valori devono essere visualizzati nelle etichette dei dati. Il valore predefinito è **false**. |
| [get_Top](./get_top/)() | Ottiene o imposta la distanza dell'etichetta dei dati in punti dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [Position](./get_position/), a seconda del valore della proprietà [TopMode](./get_topmode/). |
| [get_TopMode](./get_topmode/)() | Ottiene o imposta la modalità di interpretazione del valore della proprietà [Top](./get_top/): se imposta la posizione dell'etichetta dei dati dal bordo superiore del grafico o dalla posizione specificata dalla sua proprietà [Position](./get_position/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Ottiene/imposta un flag che indica se questa etichetta è nascosta. Il valore predefinito è **false**. |
| [set_Left](./set_left/)(double) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Left](./get_left/). |
| [set_LeftMode](./set_leftmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode](./get_leftmode/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Imposta il separatore di stringa utilizzato per le etichette dei dati in un grafico. Il valore predefinito è una virgola, eccetto per i grafici a torta che mostrano solo il nome della categoria e la percentuale, dove viene utilizzato un ritorno a capo. |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Consente di specificare se il nome della categoria deve essere visualizzato per le etichette dei dati in un grafico. Il valore predefinito è **false**. |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Consente di specificare se i valori dell'intervallo delle etichette dei dati devono essere visualizzati nelle etichette dei dati. Il valore predefinito è **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Consente di specificare se le linee guida delle etichette dei dati devono essere mostrate. Il valore predefinito è **false**. |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Consente di specificare se la chiave della legenda deve essere visualizzata per le etichette dei dati in un grafico. Il valore predefinito è **false**. |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Consente di specificare se il valore percentuale deve essere visualizzato per le etichette dei dati in un grafico. Il valore predefinito è **false**. |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Imposta un Boolean per indicare il comportamento di visualizzazione del nome della serie per le etichette dei dati in un grafico. **true** per mostrare il nome della serie; **false** per nasconderlo. Per impostazione predefinita **false**. |
| [set_ShowValue](./set_showvalue/)(bool) | Consente di specificare se i valori devono essere visualizzati nelle etichette dei dati. Il valore predefinito è **false**. |
| [set_Top](./set_top/)(double) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top](./get_top/). |
| [set_TopMode](./set_topmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode](./get_topmode/). |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
