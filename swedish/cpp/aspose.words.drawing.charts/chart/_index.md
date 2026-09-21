---
title: "Aspose::Words::Drawing::Charts::Chart klass"
linktitle: "Diagram"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::Chart klass. Ger åtkomst till diagrammets formegenskaper. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.drawing.charts/chart/
---
## Chart class


Ger åtkomst till diagrammets formegenskaper. För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class Chart : public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Axes](./get_axes/)() | Hämtar en samling av alla axlar i detta diagram. |
| [get_AxisX](./get_axisx/)() | Ger åtkomst till egenskaperna för diagrammets primära X‑axel. |
| [get_AxisY](./get_axisy/)() | Ger åtkomst till egenskaperna för diagrammets primära Y‑axel. |
| [get_AxisZ](./get_axisz/)() | Ger åtkomst till egenskaperna för diagrammets Z‑axel. |
| [get_DataTable](./get_datatable/)() | Ger åtkomst till egenskaperna för en datatabell i detta diagram. Datatabellen kan visas med egenskapen [Show](../chartdatatable/get_show/). |
| [get_Format](./get_format/)() | Ger åtkomst till fyllnings‑ och linjeformatering för diagrammet. |
| [get_Legend](./get_legend/)() | Ger åtkomst till diagrammets förklaringsruta‑egenskaper. |
| [get_Series](./get_series/)() | Tillhandahåller åtkomst till seriekollektionen. |
| [get_SeriesGroups](./get_seriesgroups/)() | Tillhandahåller åtkomst till en seriegropps-samling för detta diagram. |
| [get_SourceFullName](./get_sourcefullname/)() | Hämtar sökvägen och namnet på en xls/xlsx-fil som detta diagram är länkat till. |
| [get_Style](./get_style/)() | Hämtar diagrammets stil. |
| [get_Title](./get_title/)() | Tillhandahåller åtkomst till diagrammets titelsegenskaper. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::Charts::Chart::get_SourceFullName](./get_sourcefullname/). |
| [set_Style](./set_style/)(Aspose::Words::Drawing::Charts::ChartStyle) | Ställer in diagrammets stil. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man infogar ett diagram och anger en titel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en diagramform med en dokumentbyggare och hämta dess diagram.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Använd egenskapen "Title" för att ge vårt diagram en titel, som visas i diagramområdets övre centrum.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Ställ in egenskapen "Show" till "true" för att göra titeln synlig.
title->set_Show(true);

// Ställ in egenskapen "Overlay" till "true" för att ge andra diagramelement mer utrymme genom att låta dem överlappa titeln.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
