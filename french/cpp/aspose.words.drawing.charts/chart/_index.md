---
title: "Aspose::Words::Drawing::Charts::Chart class"
linktitle: "Graphique"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Drawing::Charts::Chart. Fournit l'accès aux propriétés de la forme du graphique. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.drawing.charts/chart/
---
## Chart class


Fournit l'accès aux propriétés de la forme du graphique. Pour en savoir plus, consultez l'article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class Chart : public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Axes](./get_axes/)() | Obtient une collection de tous les axes de ce graphique. |
| [get_AxisX](./get_axisx/)() | Fournit l'accès aux propriétés de l'axe X principal du graphique. |
| [get_AxisY](./get_axisy/)() | Fournit l'accès aux propriétés de l'axe Y principal du graphique. |
| [get_AxisZ](./get_axisz/)() | Fournit l'accès aux propriétés de l'axe Z du graphique. |
| [get_DataTable](./get_datatable/)() | Fournit l'accès aux propriétés d'un tableau de données de ce graphique. Le tableau de données peut être affiché en utilisant la propriété [Show](../chartdatatable/get_show/). |
| [get_Format](./get_format/)() | Fournit l'accès au format de remplissage et de ligne du graphique. |
| [get_Legend](./get_legend/)() | Fournit l'accès aux propriétés de la légende du graphique. |
| [get_Series](./get_series/)() | Fournit l'accès à la collection de séries. |
| [get_SeriesGroups](./get_seriesgroups/)() | Fournit l'accès à une collection de groupes de séries de ce graphique. |
| [get_SourceFullName](./get_sourcefullname/)() | Obtient le chemin et le nom d'un fichier xls/xlsx auquel ce graphique est lié. |
| [get_Style](./get_style/)() | Obtient le style du graphique. |
| [get_Title](./get_title/)() | Fournit l'accès aux propriétés du titre du graphique. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::Charts::Chart::get_SourceFullName](./get_sourcefullname/). |
| [set_Style](./set_style/)(Aspose::Words::Drawing::Charts::ChartStyle) | Définit le style du graphique. |
| static [Type](./type/)() |  |

## Exemples



Montre comment insérer un graphique et définir un titre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une forme de graphique avec un constructeur de document et récupérez son graphique.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Utilisez la propriété "Title" pour donner à notre graphique un titre, qui apparaît au centre supérieur de la zone du graphique.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Définissez la propriété "Show" sur "true" pour rendre le titre visible.
title->set_Show(true);

// Définissez la propriété "Overlay" sur "true". Donnez plus d'espace aux autres éléments du graphique en leur permettant de chevaucher le titre.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
