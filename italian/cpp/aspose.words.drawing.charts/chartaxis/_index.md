---
title: "Aspose::Words::Drawing::Charts::ChartAxis classe"
linktitle: "ChartAxis"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis classe. Rappresenta le opzioni dell'asse del grafico. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class


Rappresenta le opzioni dell'asse del grafico. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxis : public Aspose::Words::Drawing::Charts::Core::IDmlChartTitleHolder,
                  public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                  public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                  public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AxisBetweenCategories](./get_axisbetweencategories/)() | Ottiene o imposta un flag che indica se l'asse dei valori attraversa l'asse delle categorie tra le categorie. |
| [get_BaseTimeUnit](./get_basetimeunit/)() | Restituisce o imposta l'unità di tempo più piccola rappresentata sull'asse delle categorie temporali. |
| [get_CategoryType](./get_categorytype/)() | Ottiene o imposta il tipo dell'asse delle categorie. |
| [get_Crosses](./get_crosses/)() | Specifica come questo asse attraversa l'asse perpendicolare. |
| [get_CrossesAt](./get_crossesat/)() | Specifica dove sull'asse perpendicolare l'asse attraversa. |
| [get_DisplayUnit](./get_displayunit/)() | Specifica il valore di scala delle unità di visualizzazione per l'asse dei valori. |
| [get_Document](./get_document/)() | Restituisce il documento che contiene il grafico padre. |
| [get_Format](./get_format/)() | Fornisce l'accesso alla formattazione delle linee dell'asse e al riempimento delle etichette dei tick. |
| [get_HasMajorGridlines](./get_hasmajorgridlines/)() | Ottiene o imposta un flag che indica se l'asse ha linee di griglia principali. |
| [get_HasMinorGridlines](./get_hasminorgridlines/)() | Ottiene o imposta un flag che indica se l'asse ha linee di griglia secondarie. |
| [get_Hidden](./get_hidden/)() | Ottiene o imposta un flag che indica se questo asse è nascosto o meno. |
| [get_MajorTickMark](./get_majortickmark/)() | Restituisce o imposta i segni principali. |
| [get_MajorUnit](./get_majorunit/)() | Restituisce o imposta la distanza tra i segni principali. |
| [get_MajorUnitIsAuto](./get_majorunitisauto/)() | Ottiene o imposta un flag che indica se deve essere utilizzata la distanza predefinita tra i segni principali. |
| [get_MajorUnitScale](./get_majorunitscale/)() | Restituisce o imposta il valore di scala per i segni principali sull'asse delle categorie temporali. |
| [get_MinorTickMark](./get_minortickmark/)() | Restituisce o imposta i segni secondari per l'asse. |
| [get_MinorUnit](./get_minorunit/)() | Restituisce o imposta la distanza tra i segni secondari. |
| [get_MinorUnitIsAuto](./get_minorunitisauto/)() | Ottiene o imposta un flag che indica se deve essere utilizzata la distanza predefinita tra i segni secondari. |
| [get_MinorUnitScale](./get_minorunitscale/)() | Restituisce o imposta il valore di scala per i segni secondari sull'asse delle categorie temporali. |
| [get_NumberFormat](./get_numberformat/)() | Restituisce un oggetto [ChartNumberFormat](../chartnumberformat/) che consente di definire i formati numerici per l'asse. |
| [get_ReverseOrder](./get_reverseorder/)() | Restituisce o imposta un flag che indica se i valori dell'asse devono essere visualizzati in ordine inverso, cioè da max a min. |
| [get_Scaling](./get_scaling/)() | Fornisce l'accesso alle opzioni di scala dell'asse. |
| [get_TickLabels](./get_ticklabels/)() | Fornisce l'accesso alle proprietà delle etichette dei segni di graduazione dell'asse. |
| [get_TickMarkSpacing](./get_tickmarkspacing/)() | Ottiene o imposta l'intervallo al quale vengono disegnati i segni di graduazione. |
| [get_Title](./get_title/)() | Fornisce l'accesso alle proprietà del titolo dell'asse. |
| [get_Type](./get_type/)() const | Restituisce il tipo dell'asse. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisBetweenCategories](./set_axisbetweencategories/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_AxisBetweenCategories](./get_axisbetweencategories/). |
| [set_BaseTimeUnit](./set_basetimeunit/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_BaseTimeUnit](./get_basetimeunit/). |
| [set_CategoryType](./set_categorytype/)(Aspose::Words::Drawing::Charts::AxisCategoryType) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_CategoryType](./get_categorytype/). |
| [set_Crosses](./set_crosses/)(Aspose::Words::Drawing::Charts::AxisCrosses) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_Crosses](./get_crosses/). |
| [set_CrossesAt](./set_crossesat/)(double) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt](./get_crossesat/). |
| [set_HasMajorGridlines](./set_hasmajorgridlines/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines](./get_hasmajorgridlines/). |
| [set_HasMinorGridlines](./set_hasminorgridlines/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_HasMinorGridlines](./get_hasminorgridlines/). |
| [set_Hidden](./set_hidden/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden](./get_hidden/). |
| [set_MajorTickMark](./set_majortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorTickMark](./get_majortickmark/). |
| [set_MajorUnit](./set_majorunit/)(double) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnit](./get_majorunit/). |
| [set_MajorUnitIsAuto](./set_majorunitisauto/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitIsAuto](./get_majorunitisauto/). |
| [set_MajorUnitScale](./set_majorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_MajorUnitScale](./get_majorunitscale/). |
| [set_MinorTickMark](./set_minortickmark/)(Aspose::Words::Drawing::Charts::AxisTickMark) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorTickMark](./get_minortickmark/). |
| [set_MinorUnit](./set_minorunit/)(double) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnit](./get_minorunit/). |
| [set_MinorUnitIsAuto](./set_minorunitisauto/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto](./get_minorunitisauto/). |
| [set_MinorUnitScale](./set_minorunitscale/)(Aspose::Words::Drawing::Charts::AxisTimeUnit) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitScale](./get_minorunitscale/). |
| [set_ReverseOrder](./set_reverseorder/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_ReverseOrder](./get_reverseorder/). |
| [set_TickMarkSpacing](./set_tickmarkspacing/)(int32_t) | Impostatore per [Aspose::Words::Drawing::Charts::ChartAxis::get_TickMarkSpacing](./get_tickmarkspacing/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come inserire un grafico e modificare l'aspetto dei suoi assi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart->get_Series()->Clear();

// Inserisci una serie di grafico con categorie per l'asse X e i rispettivi valori numerici per l'asse Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// Gli assi del grafico hanno varie opzioni che possono modificare il loro aspetto,
// come la loro direzione, le tacche delle unità maggiori/minori e i segni di spunta.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Category);
xAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

ASPOSE_ASSERT_EQ(doc, xAxis->get_Document());

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Automatic);
yAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
yAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::NextToAxis);
yAxis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
yAxis->get_TickLabels()->get_Font()->set_Color(System::Drawing::Color::get_Red());
yAxis->get_TickLabels()->set_Spacing(1);

// I grafici a colonne non hanno un asse Z.
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
