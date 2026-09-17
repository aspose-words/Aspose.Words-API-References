---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle classe"
linktitle: "ChartAxisTitle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle classe. Fournit l'accès aux propriétés du titre de l'axe. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 5750
url: /fr/cpp/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class


Fournit l'accès aux propriétés du titre d'axe. Pour en savoir plus, consultez l'article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxisTitle : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Font](./get_font/)() | Fournit l'accès au formatage de police du titre de l'axe. |
| [get_Format](./get_format/)() | Fournit l'accès au formatage du remplissage et de la ligne du titre de l'axe. |
| [get_Orientation](./get_orientation/)() | Obtient ou définit l'orientation du texte du titre de l'axe. |
| [get_Overlay](./get_overlay/)() | Détermine si d'autres éléments du graphique sont autorisés à chevaucher le titre. La valeur par défaut est **false**. |
| [get_Rotation](./get_rotation/)() | Obtient ou définit la rotation du titre de l'axe en degrés. |
| [get_Show](./get_show/)() | Détermine si le titre doit être affiché pour l'axe. La valeur par défaut est **false**. |
| [get_Text](./get_text/)() | Obtient ou définit le texte du titre de l'axe. Si **null** ou une valeur vide est spécifiée, un titre généré automatiquement sera affiché. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment définir le titre de l'axe du graphique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Supprimer la série générée par défaut.
seriesColl->Clear();

seriesColl->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"}), System::MakeArray<double>({1, 2}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisXTitle = chart->get_AxisX()->get_Title();
chartAxisXTitle->set_Text(u"Categories");
chartAxisXTitle->set_Show(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisYTitle = chart->get_AxisY()->get_Title();
chartAxisYTitle->set_Text(u"Values");
chartAxisYTitle->set_Show(true);
chartAxisYTitle->set_Overlay(true);
chartAxisYTitle->get_Font()->set_Size(12);
chartAxisYTitle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.ChartAxisTitle.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
