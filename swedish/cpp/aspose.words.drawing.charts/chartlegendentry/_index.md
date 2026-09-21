---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry class"
linktitle: "ChartLegendEntry"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry klass. Representerar ett diagramförklaringspost. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class


Representerar ett diagramförklaringspost. För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegendEntry : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                         public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Font](./get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för detta förklaringspost. |
| [get_IsHidden](./get_ishidden/)() const | Hämtar eller anger ett värde som indikerar om detta inlägg är dolt i diagramförklaringen. Standardvärdet är **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden](./get_ishidden/). |
| static [Type](./type/)() |  |
## Anmärkningar


En förklaringspost motsvarar en specifik diagramserie eller trendlinje.

Texten för posten är namnet på serien eller trendlinjen. Texten kan inte ändras.

## Exempel



Visar hur man arbetar med ett förklaringsteckensnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// Ställ in standardteckenstorlek för alla förklaringsposter.
chartLegend->get_Font()->set_Size(14);
// Ändra teckensnitt för en specifik förklaringspost.
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// Hämta förklaringspost för diagramserie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
