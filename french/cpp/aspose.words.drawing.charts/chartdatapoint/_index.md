---
title: "Aspose::Words::Drawing::Charts::ChartDataPoint class"
linktitle: "ChartDataPoint"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartDataPoint class. Permet de spécifier le formatage d'un seul point de données sur le graphique. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


Permet de spécifier le formatage d'un seul point de données sur le graphique. Pour en savoir plus, consultez l'article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataPoint : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormat](./clearformat/)() | Efface le format de ce point de données. Les propriétés sont définies aux valeurs par défaut définies dans la série parente. |
| [get_Bubble3D](./get_bubble3d/)() override | Spécifie si les bulles dans le graphique à bulles doivent avoir un effet 3D appliqué. |
| [get_Explosion](./get_explosion/)() override | Spécifie la distance à laquelle le point de données doit être déplacé depuis le centre du secteur. Peut être négatif, un négatif signifie que la propriété n'est pas définie et qu'aucune explosion ne doit être appliquée. S'applique uniquement aux graphiques en secteurs. |
| [get_Format](./get_format/)() | Fournit l'accès au remplissage et au formatage des lignes de ce point de données. |
| [get_Index](./get_index/)() | Indice du point de données auquel cet objet applique le formatage. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Spécifie si l'élément parent doit inverser ses couleurs si la valeur est négative. |
| [get_Marker](./get_marker/)() override | Spécifie le marqueur de données du graphique. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Spécifie si les bulles dans le graphique à bulles doivent avoir un effet 3D appliqué. |
| [set_Explosion](./set_explosion/)(int32_t) override | Définisseur pour [Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion](./get_explosion/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Spécifie si l'élément parent doit inverser ses couleurs si la valeur est négative. |
| static [Type](./type/)() |  |
## Voir aussi

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
