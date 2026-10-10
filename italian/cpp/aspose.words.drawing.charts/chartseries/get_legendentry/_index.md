---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_LegendEntry metodo"
linktitle: "get_LegendEntry"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_LegendEntry metodo. Ottiene una voce di legenda per questa serie di grafico in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.drawing.charts/chartseries/get_legendentry/
---
## ChartSeries::get_LegendEntry method


Ottiene una voce della legenda per questa serie di grafico.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> Aspose::Words::Drawing::Charts::ChartSeries::get_LegendEntry()
```


## Esempi



Mostra come lavorare con un carattere della legenda.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// Imposta la dimensione predefinita del carattere per tutte le voci della legenda.
chartLegend->get_Font()->set_Size(14);
// Cambia il carattere per una voce specifica della legenda.
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// Ottieni la voce della legenda per la serie del grafico.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## Vedi anche

* Class [ChartLegendEntry](../../chartlegendentry/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
