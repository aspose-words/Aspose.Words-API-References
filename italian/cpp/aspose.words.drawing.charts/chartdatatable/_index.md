---
title: "Aspose::Words::Drawing::Charts::ChartDataTable class"
linktitle: "ChartDataTable"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Drawing::Charts::ChartDataTable. Consente di specificare le proprietà di una tabella dati del grafico in C++."
type: docs
weight: 9500
url: /it/cpp/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class


Consente di specificare le proprietà di una tabella dati del grafico.

```cpp
class ChartDataTable : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Font](./get_font/)() | Fornisce l'accesso alla formattazione del carattere della tabella dati. |
| [get_Format](./get_format/)() | Fornisce l'accesso al riempimento dello sfondo del testo e alla formattazione del bordo della tabella dati. |
| [get_HasHorizontalBorder](./get_hashorizontalborder/)() const | Ottiene o imposta un flag che indica se un bordo orizzontale della tabella dati è visualizzato. Il valore predefinito è **true**. |
| [get_HasLegendKeys](./get_haslegendkeys/)() const | Ottiene o imposta un flag che indica se le chiavi della legenda sono visualizzate nella tabella dati. Il valore predefinito è **true**. |
| [get_HasOutlineBorder](./get_hasoutlineborder/)() const | Ottiene o imposta un flag che indica se un bordo di contorno, cioè un bordo attorno ai nomi delle serie e delle categorie, è visualizzato. Il valore predefinito è **true**. |
| [get_HasVerticalBorder](./get_hasverticalborder/)() const | Ottiene o imposta un flag che indica se un bordo verticale della tabella dati è visualizzato. Il valore predefinito è **true**. |
| [get_Show](./get_show/)() const | Ottiene o imposta un flag che indica se la tabella dati verrà mostrata per il grafico. Il valore predefinito è **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_HasHorizontalBorder](./set_hashorizontalborder/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasHorizontalBorder](./get_hashorizontalborder/). |
| [set_HasLegendKeys](./set_haslegendkeys/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasLegendKeys](./get_haslegendkeys/). |
| [set_HasOutlineBorder](./set_hasoutlineborder/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder](./get_hasoutlineborder/). |
| [set_HasVerticalBorder](./set_hasverticalborder/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasVerticalBorder](./get_hasverticalborder/). |
| [set_Show](./set_show/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartDataTable::get_Show](./get_show/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come visualizzare la tabella dati con i dati delle serie del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();
auto xValues = System::MakeArray<double>({2020, 2021, 2022, 2023});
series->Add(u"Series1", xValues, System::MakeArray<double>({5, 11, 2, 7}));
series->Add(u"Series2", xValues, System::MakeArray<double>({6, 5.5, 7, 7.8}));
series->Add(u"Series3", xValues, System::MakeArray<double>({10, 8, 7, 9}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataTable> dataTable = chart->get_DataTable();
dataTable->set_Show(true);

dataTable->set_HasLegendKeys(false);
dataTable->set_HasHorizontalBorder(false);
dataTable->set_HasVerticalBorder(false);
dataTable->set_HasOutlineBorder(false);

dataTable->get_Font()->set_Italic(true);
dataTable->get_Format()->get_Stroke()->set_Weight(1);
dataTable->get_Format()->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDot);
dataTable->get_Format()->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());

doc->Save(get_ArtifactsDir() + u"Charts.DataTable.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
