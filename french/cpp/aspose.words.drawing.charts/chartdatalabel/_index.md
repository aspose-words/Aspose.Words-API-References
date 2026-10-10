---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel class"
linktitle: "ChartDataLabel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel class. Représente une étiquette de données sur un point de graphique ou une ligne de tendance. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class


Représente l'étiquette de données sur un point de graphique ou une ligne de tendance. Pour en savoir plus, consultez l'article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabel : public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                       public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormat](./clearformat/)() | Efface le format de cette étiquette de données. Les propriétés sont définies aux valeurs par défaut définies dans la collection d’étiquettes de données parente. |
| [get_Font](./get_font/)() | Fournit l’accès au formatage de police de cette étiquette de données. |
| [get_Format](./get_format/)() | Fournit l’accès au formatage du remplissage et du trait de l’étiquette de données. |
| [get_Index](./get_index/)() | Spécifie l’index de l’élément contenant. Cet index détermine à quelle collection d’enfants du parent cet élément s’applique. La valeur par défaut est 0. |
| [get_IsHidden](./get_ishidden/)() | Obtient/definit un indicateur indiquant si cette étiquette est masquée. La valeur par défaut est **false**. |
| [get_IsVisible](./get_isvisible/)() | Renvoie **true** si cette étiquette de données a quelque chose à afficher. |
| [get_Left](./get_left/)() | Obtient ou définit la distance de l’étiquette de données en points depuis le bord gauche du graphique ou depuis la position spécifiée par sa propriété [Position](./get_position/), selon la valeur de la propriété [LeftMode](./get_leftmode/). |
| [get_LeftMode](./get_leftmode/)() | Obtient ou définit le mode d’interprétation de la valeur de la propriété [Left](./get_left/) : si elle définit l’emplacement de l’étiquette de données depuis le bord gauche du graphique ou depuis la position spécifiée par sa propriété [Position](./get_position/). |
| [get_NumberFormat](./get_numberformat/)() | Renvoie le format numérique de l’élément parent. |
| [get_Orientation](./get_orientation/)() | Obtient ou définit l’orientation du texte de l’étiquette. |
| [get_Position](./get_position/)() | Obtient ou définit la position de l’étiquette de données. |
| [get_Rotation](./get_rotation/)() | Obtient ou définit la rotation de l’étiquette en degrés. |
| [get_Separator](./get_separator/)() | Obtient le séparateur de chaîne utilisé pour les étiquettes de données sur un graphique. La valeur par défaut est une virgule, sauf pour les graphiques circulaires affichant uniquement le nom de catégorie et le pourcentage, où un saut de ligne doit être utilisé à la place. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Permet de spécifier si la taille de la bulle doit être affichée pour les étiquettes de données sur un graphique. S’applique uniquement aux graphiques à bulles. La valeur par défaut est **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Permet de spécifier si le nom de catégorie doit être affiché pour les étiquettes de données sur un graphique. La valeur par défaut est **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Permet de spécifier si les valeurs de la plage des étiquettes de données doivent être affichées dans les étiquettes de données. La valeur par défaut est **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Permet de spécifier si les lignes de repère des étiquettes de données doivent être affichées. La valeur par défaut est **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Permet de spécifier si la clé de légende doit être affichée pour les étiquettes de données sur un graphique. La valeur par défaut est **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Permet de spécifier si la valeur de pourcentage doit être affichée pour les étiquettes de données sur un graphique. La valeur par défaut est **false**. |
| [get_ShowSeriesName](./get_showseriesname/)() | Renvoie un booléen indiquant le comportement d'affichage du nom de série pour les étiquettes de données sur un graphique. **true** pour afficher le nom de la série ; **false** pour le masquer. Par défaut **false**. |
| [get_ShowValue](./get_showvalue/)() | Permet de spécifier si les valeurs doivent être affichées dans les étiquettes de données. La valeur par défaut est **false**. |
| [get_Top](./get_top/)() | Obtient ou définit la distance de l'étiquette de données en points par rapport au bord supérieur du graphique ou à la position spécifiée par sa propriété [Position](./get_position/), selon la valeur de la propriété [TopMode](./get_topmode/). |
| [get_TopMode](./get_topmode/)() | Obtient ou définit le mode d'interprétation de la valeur de la propriété [Top](./get_top/) : si elle définit l'emplacement de l'étiquette de données à partir du bord supérieur du graphique ou à partir de la position spécifiée par sa propriété [Position](./get_position/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Obtient/definit un indicateur indiquant si cette étiquette est masquée. La valeur par défaut est **false**. |
| [set_Left](./set_left/)(double) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Left](./get_left/). |
| [set_LeftMode](./set_leftmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode](./get_leftmode/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Définit le séparateur de chaîne utilisé pour les étiquettes de données sur un graphique. La valeur par défaut est une virgule, sauf pour les graphiques circulaires affichant uniquement le nom de catégorie et le pourcentage, où un saut de ligne doit être utilisé à la place. |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Permet de spécifier si le nom de catégorie doit être affiché pour les étiquettes de données sur un graphique. La valeur par défaut est **false**. |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Permet de spécifier si les valeurs de la plage des étiquettes de données doivent être affichées dans les étiquettes de données. La valeur par défaut est **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Permet de spécifier si les lignes de repère des étiquettes de données doivent être affichées. La valeur par défaut est **false**. |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Permet de spécifier si la clé de légende doit être affichée pour les étiquettes de données sur un graphique. La valeur par défaut est **false**. |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Permet de spécifier si la valeur de pourcentage doit être affichée pour les étiquettes de données sur un graphique. La valeur par défaut est **false**. |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Définit un booléen indiquant le comportement d'affichage du nom de série pour les étiquettes de données sur un graphique. **true** pour afficher le nom de la série ; **false** pour le masquer. Par défaut **false**. |
| [set_ShowValue](./set_showvalue/)(bool) | Permet de spécifier si les valeurs doivent être affichées dans les étiquettes de données. La valeur par défaut est **false**. |
| [set_Top](./set_top/)(double) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top](./get_top/). |
| [set_TopMode](./set_topmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode](./get_topmode/). |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
