---
title: "Metodo Aspose::Words::Drawing::Charts::ChartLegend::get_Font"
linktitle: "get_Font"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::ChartLegend::get_Font. Fornisce l'accesso alla formattazione predefinita del carattere delle voci della legenda. Per sovrascrivere la formattazione del carattere per una voce specifica della legenda, utilizzare la proprietà Font in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing.charts/chartlegend/get_font/
---
## ChartLegend::get_Font method


Fornisce l'accesso alla formattazione predefinita del carattere delle voci della legenda. Per sovrascrivere la formattazione del carattere per una voce specifica della legenda, utilizzare la proprietà [Font](../../chartlegendentry/get_font/).

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartLegend::get_Font()
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

* Class [Font](../../../aspose.words/font/)
* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
