---
title: "Aspose::Words::Drawing::Charts::ChartSeries classe"
linktitle: "ChartSeries"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries classe. Représente les propriétés de la série de graphique. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class


Représente les propriétés de la série de graphique. Pour en savoir plus, consultez l'article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartSeries : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                    public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Ajoute la valeur X spécifiée à la série du graphique. Si la série prend en charge les valeurs Y et les tailles de bulles, elles seront vides pour la valeur X. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Ajoute les valeurs X et Y spécifiées à la série du graphique. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Ajoute la valeur X spécifiée, la valeur Y et la taille de la bulle à la série du graphique. |
| [Clear](./clear/)() | Supprime toutes les valeurs de données de la série du graphique. Le format de tous les points de données individuels et des étiquettes de données est réinitialisé. |
| [ClearValues](./clearvalues/)() | Supprime toutes les valeurs de données de la série du graphique tout en préservant le format des points de données et des étiquettes de données. |
| [CopyFormatFrom](./copyformatfrom/)(int32_t) | Copie le format de point de données par défaut depuis le point de données avec l'index spécifié. |
| [get_Bubble3D](./get_bubble3d/)() override | Spécifie si les bulles dans le graphique à bulles doivent avoir un effet 3D appliqué. |
| [get_BubbleSizes](./get_bubblesizes/)() | Obtient une collection de tailles de bulles pour cette série de graphique. |
| [get_DataLabels](./get_datalabels/)() | Spécifie les paramètres des étiquettes de données pour l'ensemble de la série. |
| [get_DataPoints](./get_datapoints/)() const | Renvoie une collection d'objets de formatage pour tous les points de données de cette série. |
| [get_Explosion](./get_explosion/)() override | Spécifie la distance à laquelle le point de données doit être déplacé depuis le centre du secteur. Peut être négatif, un négatif signifie que la propriété n'est pas définie et qu'aucune explosion ne doit être appliquée. S'applique uniquement aux graphiques en secteurs. |
| [get_Format](./get_format/)() | Fournit l'accès au remplissage et au formatage des lignes de la série. |
| [get_HasDataLabels](./get_hasdatalabels/)() const | Obtient ou définit un indicateur indiquant si les étiquettes de données sont affichées pour la série. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Spécifie si l'élément parent doit inverser ses couleurs si la valeur est négative. |
| [get_LegendEntry](./get_legendentry/)() | Obtient une entrée de légende pour cette série de graphique. |
| [get_Marker](./get_marker/)() override | Spécifie un marqueur de données. Le marqueur est créé automatiquement lorsqu'il est demandé. |
| [get_Name](./get_name/)() | Obtient le nom de la série, si le nom n'est pas défini explicitement il est généré à l'aide de l'index. Par défaut, il renvoie Série plus un basé sur l'index. |
| [get_SeriesType](./get_seriestype/)() | Obtient le type de cette série de graphique. |
| [get_Smooth](./get_smooth/)() const | Permet de spécifier si la ligne reliant les points du graphique doit être lissée à l'aide de splines Catmull-Rom. |
| [get_XValues](./get_xvalues/)() | Obtient une collection de valeurs X pour cette série de graphique. |
| [get_YValues](./get_yvalues/)() | Obtient une collection de valeurs Y pour cette série de graphique. |
| [GetType](./gettype/)() const override |  |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Insère la valeur X spécifiée dans la série de graphique à l'index indiqué. Si la série prend en charge les valeurs Y et les tailles de bulles, elles seront vides pour la valeur X. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Insère les valeurs X et Y spécifiées dans la série de graphique à l'index indiqué. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Insère la valeur X spécifiée, la valeur Y et la taille de la bulle dans la série de graphique à l'index indiqué. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Supprime la valeur X, la valeur Y et la taille de la bulle, si prises en charge, de la série de graphique à l'index indiqué. Le point de données et l'étiquette de données correspondants sont également supprimés. |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Mutateur pour [Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D](./get_bubble3d/). |
| [set_Explosion](./set_explosion/)(int32_t) override | Spécifie la distance à laquelle le point de données doit être déplacé depuis le centre du secteur. Peut être négatif, un négatif signifie que la propriété n'est pas définie et qu'aucune explosion ne doit être appliquée. S'applique uniquement aux graphiques en secteurs. |
| [set_HasDataLabels](./set_hasdatalabels/)(bool) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels](./get_hasdatalabels/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Spécifie si l'élément parent doit inverser ses couleurs si la valeur est négative. |
| [set_Name](./set_name/)(const System::String\&) | Définit le nom de la série, si le nom n'est pas défini explicitement il est généré à l'aide de l'index. Par défaut, il renvoie Série plus un basé sur l'index. |
| [set_Smooth](./set_smooth/)(bool) | Permet de spécifier si la ligne reliant les points du graphique doit être lissée à l'aide de splines Catmull-Rom. |
| static [Type](./type/)() |  |
## Voir aussi

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
