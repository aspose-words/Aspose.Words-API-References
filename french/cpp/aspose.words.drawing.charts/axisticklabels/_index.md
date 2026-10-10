---
title: "Aspose::Words::Drawing::Charts::AxisTickLabels class"
linktitle: "AxisTickLabels"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Charts::AxisTickLabels class. Représente les propriétés des étiquettes de marques d'axe en C++."
type: docs
weight: 3250
url: /fr/cpp/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class


Représente les propriétés des libellés des marques de graduation de l'axe.

```cpp
class AxisTickLabels : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Obtient ou définit l'alignement du texte des étiquettes de marques d'axe. |
| [get_Font](./get_font/)() | Fournit l'accès au format de police des étiquettes de marques. |
| [get_IsAutoSpacing](./get_isautospacing/)() | Obtient ou définit un indicateur indiquant s'il faut utiliser un intervalle automatique pour le rendu des étiquettes de marques. |
| [get_Offset](./get_offset/)() | Obtient ou définit la distance des étiquettes de marques par rapport à l'axe. |
| [get_Orientation](./get_orientation/)() | Obtient ou définit l'orientation du texte des étiquettes de marques. |
| [get_Position](./get_position/)() | Obtient ou définit la position des étiquettes de marques sur l'axe. |
| [get_Rotation](./get_rotation/)() | Obtient ou définit la rotation des étiquettes de marques en degrés. |
| [get_Spacing](./get_spacing/)() | Obtient ou définit l'intervalle auquel les étiquettes de repère sont dessinées. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Définisseur pour [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Alignment](./get_alignment/). |
| [set_IsAutoSpacing](./set_isautospacing/)(bool) | Définisseur pour [Aspose::Words::Drawing::Charts::AxisTickLabels::get_IsAutoSpacing](./get_isautospacing/). |
| [set_Offset](./set_offset/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Offset](./get_offset/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Définisseur pour [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::AxisTickLabelPosition) | Définisseur pour [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation](./get_rotation/). |
| [set_Spacing](./set_spacing/)(int32_t) | Définisseur pour [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Spacing](./get_spacing/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment insérer un graphique et modifier l'apparence de ses axes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique vierge.
chart->get_Series()->Clear();

// Insérez une série de graphique avec des catégories pour l'axe X et les valeurs numériques respectives pour l'axe Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// Les axes du graphique offrent diverses options qui peuvent modifier leur apparence,
// telles que leur direction, les graduations principales/secondaires, et les marques de graduation.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Category);
xAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

ASPOSE_ASSERT_EQ(doc, xAxis->get_Document());

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Automatic);
yAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
yAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::NextToAxis);
yAxis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
yAxis->get_TickLabels()->get_Font()->set_Color(System::Drawing::Color::get_Red());
yAxis->get_TickLabels()->set_Spacing(1);

// Les graphiques en colonnes n'ont pas d'axe Z.
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
