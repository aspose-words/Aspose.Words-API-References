---
title: "Aspose::Words::Drawing::Charts::ChartStyle enum"
linktitle: "ChartStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartStyle enum. Anger fördefinierade stilar för ett diagram i C++."
type: docs
weight: 27875
url: /sv/cpp/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enum


Anger fördefinierade stilar för ett diagram.

```cpp
enum class ChartStyle
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Normal | 0 | Representerar standarddiagramstilen. |
| Dämpad | 1 | En stil med dämpade färger. |
| Mättad | 2 | En stil med mer mättade färger. |
| Skuggad | 3 | En stil med skuggade datapunkter. |
| Flat | 4 | En stil med platta datapunkter utan gradient. |
| Skuggad | 5 | En stil med datapunkter som har en skugga. |
| Gradient | 6 | En stil med gradientfyllning av datapunkter. |
| Original | 7 | En stil med ett originalt utseende på ett diagram. |
| Transparent1 | 8 | En stil med transparenta datapunkter. |
| Transparent2 | 9 | En stil med transparenta datapunkter. |
| Outline | 10 | En stil med datapunkter utan fyllning, men endast en kontur. |
| OutlineBlack | 11 | En stil med svart diagrambakgrund, där datapunkter saknar fyllning men bara har en kontur. |
| Svart | 12 | En stil med svart diagrambakgrund. |
| Grå | 13 | En stil med grå gradient i diagrambakgrunden. |
| Blå | 14 | En stil med blå diagrambakgrund. |
| ShadedPlot | 15 | En stil där plotområdet är skuggat. |


## Exempel



Visar hur man ställer in och hämtar diagramstil.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett diagram i den svarta stilen.
builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 250, Aspose::Words::Drawing::Charts::ChartStyle::Black);

doc->Save(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

// Hämta ett diagram för att uppdatera.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Hämta diagramstilen.
ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartStyle::Black, chart->get_Style());
```

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
