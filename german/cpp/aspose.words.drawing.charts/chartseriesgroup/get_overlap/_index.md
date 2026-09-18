---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap‑Methode"
linktitle: "get_Overlap"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap‑Methode. Gibt den Prozentsatz zurück oder setzt ihn, wie stark die Serienbalken oder -spalten in C++ überlappen."
type: docs
weight: 9000
url: /de/cpp/aspose.words.drawing.charts/chartseriesgroup/get_overlap/
---
## ChartSeriesGroup::get_Overlap method


Liest oder legt den Prozentsatz fest, wie stark die Serienbalken oder -spalten überlappen.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap()
```

## Hinweise


Gilt für Seriengruppen aller Balken‑ und Säulentypen.

Der zulässige Wertebereich liegt zwischen -100 und 100, einschließlich. Ein Wert von 0 bedeutet, dass kein Abstand zwischen Balken/Säulen besteht. Bei einem Wert von -100 ist der Abstand zwischen Balken/Säulen gleich ihrer Breite. Ein Wert von 100 bedeutet, dass die Balken/Säulen vollständig überlappen.

## Beispiele



Zeigt, wie man die Lückenbreite und Überlappung konfiguriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Setzt die Spaltenlückenbreite und Überlappung.
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## Siehe auch

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
