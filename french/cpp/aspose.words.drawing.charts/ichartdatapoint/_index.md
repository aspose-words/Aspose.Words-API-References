---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint interface"
linktitle: "IChartDataPoint"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint interface. Contient les propriétés d'un seul point de données sur le graphique en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface


Contient les propriétés d'un seul point de données sur le graphique.

```cpp
class IChartDataPoint : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| virtual [get_Bubble3D](./get_bubble3d/)() | Spécifie si les bulles dans le graphique à bulles doivent avoir un effet 3D appliqué. |
| virtual [get_Explosion](./get_explosion/)() | Spécifie la distance à laquelle le point de données doit être déplacé depuis le centre du secteur. Peut être négatif, un négatif signifie que la propriété n'est pas définie et qu'aucune explosion ne doit être appliquée. S'applique uniquement aux graphiques en secteurs. |
| virtual [get_InvertIfNegative](./get_invertifnegative/)() | Spécifie si l'élément parent doit inverser ses couleurs si la valeur est négative. |
| virtual [get_Marker](./get_marker/)() | Spécifie un marqueur de données. Le marqueur est créé automatiquement lorsqu'il est demandé. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Bubble3D](./set_bubble3d/)(bool) | Mutateur pour [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D](./get_bubble3d/). |
| virtual [set_Explosion](./set_explosion/)(int32_t) | Mutateur pour [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion](./get_explosion/). |
| virtual [set_InvertIfNegative](./set_invertifnegative/)(bool) | Spécifie si l'élément parent doit inverser ses couleurs si la valeur est négative. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
