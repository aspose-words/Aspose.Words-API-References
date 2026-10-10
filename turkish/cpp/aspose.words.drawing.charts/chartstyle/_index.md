---
title: "Aspose::Words::Drawing::Charts::ChartStyle enum"
linktitle: "ChartStyle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartStyle enum. C++'da bir grafiğin önceden tanımlanmış stillerini belirtir."
type: docs
weight: 27875
url: /tr/cpp/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enum


Bir grafiğin önceden tanımlı stillerini belirtir.

```cpp
enum class ChartStyle
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Normal | 0 | Varsayılan grafik stilini temsil eder. |
| Muted | 1 | Susturulmuş renklerle bir stil. |
| Saturated | 2 | Daha doygun renklerle bir stil. |
| Shaded | 3 | Gölgeli veri noktalarına sahip bir stil. |
| Flat | 4 | Gradyansız düz veri noktalarına sahip bir stil. |
| Shadowed | 5 | Gölgeye sahip veri noktalarıyla bir stil. |
| Gradient | 6 | Veri noktalarının gradyan dolgusuna sahip bir stil. |
| Orijinal | 7 | Grafiğin özgün görünümüne sahip bir stil. |
| Transparent1 | 8 | Şeffaf veri noktalarına sahip bir stil. |
| Transparent2 | 9 | Şeffaf veri noktalarına sahip bir stil. |
| Outline | 10 | Dolgu olmayan, sadece dış hatı olan veri noktalarına sahip bir stil. |
| OutlineBlack | 11 | Veri noktalarının dolgu olmadan sadece dış hatı olduğu, siyah grafik arka planına sahip bir stil. |
| Siyah | 12 | Siyah grafik arka planına sahip bir stil. |
| Grey | 13 | Gri gradyan grafik arka planına sahip bir stil. |
| Mavi | 14 | Mavi grafik arka planına sahip bir stil. |
| ShadedPlot | 15 | Grafik alanının gölgelendiği bir stil. |


## Örnekler



Grafik stilini ayarlama ve alma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Siyah stilinde bir grafik ekleyin.
builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 250, Aspose::Words::Drawing::Charts::ChartStyle::Black);

doc->Save(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

// Güncellenmek üzere bir grafik alın.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Grafik stilini alın.
ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartStyle::Black, chart->get_Style());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
