---
title: "Aspose::Words::Drawing::Charts::ChartLegend class"
linktitle: "ChartLegend"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartLegend class. Représente les propriétés de la légende du graphique. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class


Représente les propriétés de la légende du graphique. Pour en savoir plus, consultez l'article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegend : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                    public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Font](./get_font/)() | Fournit l'accès au formatage de police par défaut des entrées de légende. Pour remplacer le formatage de police d'une entrée de légende spécifique, utilisez le[Font](../chartlegendentry/get_font/) propriété. |
| [get_Format](./get_format/)() | Fournit l'accès au remplissage et au formatage des lignes de la légende. |
| [get_LegendEntries](./get_legendentries/)() const | Renvoie une collection d'entrées de légende pour toutes les séries et lignes de tendance du graphique parent. |
| [get_Overlay](./get_overlay/)() const | Détermine si d'autres éléments du graphique doivent être autorisés à chevaucher la légende. La valeur par défaut est **false**. |
| [get_Position](./get_position/)() | Spécifie la position de la légende sur un graphique. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Overlay](./set_overlay/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay](./get_overlay/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::LegendPosition) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartLegend::get_Position](./get_position/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment modifier l'apparence de la légende d'un graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Déplacez la légende du graphique vers le coin supérieur droit.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Donnez plus d'espace aux autres éléments du graphique, comme le tracé, en leur permettant de chevaucher la légende.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
