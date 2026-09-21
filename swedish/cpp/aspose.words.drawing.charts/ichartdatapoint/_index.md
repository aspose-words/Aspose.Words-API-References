---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint interface"
linktitle: "IChartDataPoint"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint‑gränssnitt. Innehåller egenskaper för en enskild datapunkt i diagrammet i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface


Innehåller egenskaper för en enskild datapunkt i diagrammet.

```cpp
class IChartDataPoint : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [get_Bubble3D](./get_bubble3d/)() | Anger om bubblorna i bubbeldiagrammet ska ha en 3‑D‑effekt tillämpad. |
| virtual [get_Explosion](./get_explosion/)() | Anger hur mycket datapunkten ska flyttas från mitten av pajen. Kan vara negativt, negativt betyder att egenskapen inte är satt och ingen explosion ska tillämpas. Gäller endast pajdiagram. |
| virtual [get_InvertIfNegative](./get_invertifnegative/)() | Anger om det överordnade elementet ska invertera sina färger om värdet är negativt. |
| virtual [get_Marker](./get_marker/)() | Anger en datamarkör. Markören skapas automatiskt när den begärs. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Bubble3D](./set_bubble3d/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D](./get_bubble3d/). |
| virtual [set_Explosion](./set_explosion/)(int32_t) | Sättare för [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion](./get_explosion/). |
| virtual [set_InvertIfNegative](./set_invertifnegative/)(bool) | Anger om det överordnade elementet ska invertera sina färger om värdet är negativt. |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
