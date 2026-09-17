---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry classe"
linktitle: "ChartLegendEntry"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry classe. Représente une entrée de légende de graphique. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class


Représente une entrée de légende de graphique. Pour en savoir plus, consultez l'article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegendEntry : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                         public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Font](./get_font/)() | Fournit un accès au formatage de police de cette entrée de légende. |
| [get_IsHidden](./get_ishidden/)() const | Obtient ou définit une valeur indiquant si cette entrée est masquée dans la légende du graphique. La valeur par défaut est **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden](./get_ishidden/). |
| static [Type](./type/)() |  |
## Remarques


Une entrée de légende correspond à une série de graphique ou à une ligne de tendance spécifique.

Le texte de l'entrée est le nom de la série ou de la ligne de tendance. Le texte ne peut pas être modifié.

## Exemples



Montre comment travailler avec une police de légende.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// Définir la taille de police par défaut pour toutes les entrées de légende.
chartLegend->get_Font()->set_Size(14);
// Modifier la police d'une entrée de légende spécifique.
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// Obtenir l'entrée de légende pour une série de graphique.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
