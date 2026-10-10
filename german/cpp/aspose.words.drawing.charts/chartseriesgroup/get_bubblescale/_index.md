---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale‑Methode"
linktitle: "get_BubbleScale"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale‑Methode. Gibt die Größe der Blasen zurück oder setzt sie als Prozentsatz ihrer Standardgröße in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.drawing.charts/chartseriesgroup/get_bubblescale/
---
## ChartSeriesGroup::get_BubbleScale method


Liest oder legt die Größe der Blasen als Prozentsatz ihrer Standardgröße fest.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale()
```

## Hinweise


Gilt nur für Seriengruppen der Typen [Bubble](../../chartseriestype/) und [Bubble3D](../../chartseriestype/).

Der zulässige Wertebereich liegt zwischen 0 und 300, einschließlich. Der Standardwert ist 100.

## Beispiele



Zeigen Sie, wie die Größe der Blasen festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein 3D‑Blasendiagramm ein.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Setzen Sie die Blasenskala auf 200 %.
seriesGroup->set_BubbleScale(200);

doc->Save(get_ArtifactsDir() + u"Charts.BubbleScale.docx");
```

## Siehe auch

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
