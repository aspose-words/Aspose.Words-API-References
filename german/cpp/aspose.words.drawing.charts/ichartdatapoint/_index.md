---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint Schnittstelle"
linktitle: "IChartDataPoint"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint Schnittstelle. Enthält Eigenschaften eines einzelnen Datenpunkts im Diagramm in C++."
type: docs
weight: 19000
url: /de/cpp/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface


Enthält Eigenschaften eines einzelnen Datenpunkts im Diagramm.

```cpp
class IChartDataPoint : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [get_Bubble3D](./get_bubble3d/)() | Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen. |
| virtual [get_Explosion](./get_explosion/)() | Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. Kann negativ sein; negativ bedeutet, dass die Eigenschaft nicht gesetzt ist und keine Explosionsverschiebung angewendet wird. Gilt nur für Kuchendiagramme. |
| virtual [get_InvertIfNegative](./get_invertifnegative/)() | Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist. |
| virtual [get_Marker](./get_marker/)() | Gibt einen Datenmarker an. Der Marker wird bei Bedarf automatisch erstellt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Bubble3D](./set_bubble3d/)(bool) | Setter für [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D](./get_bubble3d/). |
| virtual [set_Explosion](./set_explosion/)(int32_t) | Setter für [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion](./get_explosion/). |
| virtual [set_InvertIfNegative](./set_invertifnegative/)(bool) | Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
