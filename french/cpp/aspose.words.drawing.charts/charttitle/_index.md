---
title: "Aspose::Words::Drawing::Charts::ChartTitle classe"
linktitle: "ChartTitle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::ChartTitle classe. Fournit l'accès aux propriétés du titre du graphique. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class


Fournit l'accès aux propriétés du titre du graphique. Pour en savoir plus, consultez l'article de documentation [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartTitle : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Font](./get_font/)() | Fournit l'accès au formatage de police du titre du graphique. |
| [get_Format](./get_format/)() | Fournit l'accès au formatage de remplissage et de ligne du titre du graphique. |
| [get_Orientation](./get_orientation/)() | Obtient ou définit l'orientation du texte du titre du graphique. |
| [get_Overlay](./get_overlay/)() | Détermine si d'autres éléments du graphique sont autorisés à chevaucher le titre. Par défaut, le chevauchement est **false**. |
| [get_Rotation](./get_rotation/)() | Obtient ou définit la rotation du titre du graphique en degrés. |
| [get_Show](./get_show/)() | Détermine si le titre doit être affiché pour ce graphique. La valeur par défaut est **true**. |
| [get_Text](./get_text/)() | Obtient ou définit le texte du titre du graphique. Si la valeur **null** ou vide est spécifiée, un titre généré automatiquement sera affiché. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Mutateur pour [Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::Charts::ChartTitle::get_Text](./get_text/). |
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
