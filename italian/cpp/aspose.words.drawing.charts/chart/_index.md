---
title: "Aspose::Words::Drawing::Charts::Chart class"
linktitle: "Grafico"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::Chart class. Fornisce l'accesso alle proprietà della forma del grafico. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.drawing.charts/chart/
---
## Chart class


Fornisce l'accesso alle proprietà della forma del grafico. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class Chart : public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Axes](./get_axes/)() | Ottiene una collezione di tutti gli assi di questo grafico. |
| [get_AxisX](./get_axisx/)() | Fornisce l'accesso alle proprietà dell'asse X primario del grafico. |
| [get_AxisY](./get_axisy/)() | Fornisce l'accesso alle proprietà dell'asse Y primario del grafico. |
| [get_AxisZ](./get_axisz/)() | Fornisce l'accesso alle proprietà dell'asse Z del grafico. |
| [get_DataTable](./get_datatable/)() | Fornisce l'accesso alle proprietà di una tabella dati di questo grafico. La tabella dati può essere visualizzata utilizzando la proprietà [Show](../chartdatatable/get_show/). |
| [get_Format](./get_format/)() | Fornisce l'accesso alla formattazione di riempimento e linea del grafico. |
| [get_Legend](./get_legend/)() | Fornisce l'accesso alle proprietà della legenda del grafico. |
| [get_Series](./get_series/)() | Fornisce l'accesso alla raccolta di serie. |
| [get_SeriesGroups](./get_seriesgroups/)() | Fornisce l'accesso a una raccolta di gruppi di serie di questo grafico. |
| [get_SourceFullName](./get_sourcefullname/)() | Ottiene il percorso e il nome di un file xls/xlsx a cui questo grafico è collegato. |
| [get_Style](./get_style/)() | Ottiene lo stile del grafico. |
| [get_Title](./get_title/)() | Fornisce l'accesso alle proprietà del titolo del grafico. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Impostatore per [Aspose::Words::Drawing::Charts::Chart::get_SourceFullName](./get_sourcefullname/). |
| [set_Style](./set_style/)(Aspose::Words::Drawing::Charts::ChartStyle) | Imposta lo stile del grafico. |
| static [Type](./type/)() |  |

## Esempi



Mostra come inserire un grafico e impostare un titolo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una forma di grafico con un document builder e ottieni il suo grafico.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Usa la proprietà "Title" per dare al nostro grafico un titolo, che appare al centro superiore dell'area del grafico.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Imposta la proprietà "Show" su "true" per rendere il titolo visibile.
title->set_Show(true);

// Imposta la proprietà "Overlay" su "true" per dare più spazio agli altri elementi del grafico consentendo loro di sovrapporsi al titolo.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
