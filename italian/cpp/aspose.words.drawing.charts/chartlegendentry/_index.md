---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry classe"
linktitle: "ChartLegendEntry"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry classe. Rappresenta una voce della legenda del grafico. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class


Rappresenta una voce della legenda del grafico. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegendEntry : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                         public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Font](./get_font/)() | Fornisce l'accesso alla formattazione del carattere di questa voce della legenda. |
| [get_IsHidden](./get_ishidden/)() const | Ottiene o imposta un valore che indica se questa voce è nascosta nella legenda del grafico. Il valore predefinito è **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden](./get_ishidden/). |
| static [Type](./type/)() |  |
## Note


Una voce della legenda corrisponde a una specifica serie di grafico o linea di tendenza.

Il testo della voce è il nome della serie o della linea di tendenza. Il testo non può essere modificato.

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
