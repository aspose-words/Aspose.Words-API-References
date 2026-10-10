---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection class"
linktitle: "ChartDataLabelCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection class. Représente une collection de ChartDataLabel. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class


Représente une collection de [ChartDataLabel](../chartdatalabel/). Pour en savoir plus, consultez l'article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabelCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel>>,
                                 public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                                 public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormat](./clearformat/)() | Efface le format de tous les [ChartDataLabel](../chartdatalabel/) de cette collection. |
| [get_Count](./get_count/)() | Renvoie le nombre de [ChartDataLabel](../chartdatalabel/) dans cette collection. |
| [get_Font](./get_font/)() | Fournit l'accès au formatage de police des étiquettes de données de la série entière. |
| [get_Format](./get_format/)() | Fournit l'accès au formatage de remplissage et de ligne des étiquettes de données. |
| [get_NumberFormat](./get_numberformat/)() | Obtient une instance de [ChartNumberFormat](../chartnumberformat/) permettant de définir le format numérique des étiquettes de données de la série entière. |
| [get_Orientation](./get_orientation/)() | Obtient ou définit l'orientation du texte des étiquettes de données de la série entière. |
| [get_Position](./get_position/)() | Obtient ou définit la position des étiquettes de données. |
| [get_Rotation](./get_rotation/)() | Obtient ou définit la rotation des étiquettes de données de la série entière en degrés. |
| [get_Separator](./get_separator/)() | Obtient ou définit le séparateur de chaîne utilisé pour les étiquettes de données de la série entière. La valeur par défaut est une virgule, sauf pour les graphiques circulaires affichant uniquement le nom de catégorie et le pourcentage, où un saut de ligne doit être utilisé à la place. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Permet de spécifier si la taille de la bulle doit être affichée pour les étiquettes de données de la série entière. S'applique uniquement aux graphiques à bulles. La valeur par défaut est **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Permet de spécifier si le nom de catégorie doit être affiché pour les étiquettes de données de la série entière. La valeur par défaut est **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Permet de spécifier si les valeurs de la plage des étiquettes de données doivent être affichées dans les étiquettes de données de la série entière. La valeur par défaut est **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Permet de spécifier si les lignes de repère des étiquettes de données doivent être affichées pour les étiquettes de données de la série entière. La valeur par défaut est **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Permet de spécifier si la clé de légende doit être affichée pour les étiquettes de données de la série entière. La valeur par défaut est **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Permet de spécifier si la valeur en pourcentage doit être affichée pour les étiquettes de données de la série entière. La valeur par défaut est **false**. S'applique uniquement aux graphiques circulaires. |
| [get_ShowSeriesName](./get_showseriesname/)() | Renvoie ou définit un booléen indiquant le comportement d'affichage du nom de la série pour les étiquettes de données de la série entière. **true** pour afficher le nom de la série ; **false** pour le masquer. Par défaut **false**. |
| [get_ShowValue](./get_showvalue/)() | Permet de spécifier si les valeurs doivent être affichées dans les étiquettes de données de la série entière. La valeur par défaut est **false**. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Renvoie [ChartDataLabel](../chartdatalabel/) pour l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator](./get_separator/). |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Définisseur de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Définisseur de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName](./get_showcategoryname/). |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Permet de spécifier si les valeurs de la plage des étiquettes de données doivent être affichées dans les étiquettes de données de la série entière. La valeur par défaut est **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Définisseur de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines](./get_showleaderlines/). |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Définisseur de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey](./get_showlegendkey/). |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Définisseur de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage](./get_showpercentage/). |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Définisseur de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName](./get_showseriesname/). |
| [set_ShowValue](./set_showvalue/)(bool) | Définisseur de [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue](./get_showvalue/). |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
