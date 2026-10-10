---
title: "Aspose::Words::Drawing::Stroke classe"
linktitle: "Stroke"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Stroke classe. Définit un trait pour une forme. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.drawing/stroke/
---
## Stroke class


Définit un trait pour une forme. Pour en savoir plus, consultez l'article de documentation [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) .

```cpp
class Stroke : public Aspose::Words::Drawing::Core::IFillable
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Obtient ou définit la couleur d'arrière-plan du trait. |
| [get_BackThemeColor](./get_backthemecolor/)() | Obtient ou définit un objet ThemeColor qui représente la couleur d'arrière-plan du trait. |
| [get_BackTintAndShade](./get_backtintandshade/)() | Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan du trait. |
| [get_BaseForeColor](./get_baseforecolor/)() | Obtient la couleur de premier plan de base du trait sans aucun modificateur. |
| [get_Color](./get_color/)() | Définit la couleur d'un trait. |
| [get_Color2](./get_color2/)() | Définit une seconde couleur pour un trait. |
| [get_DashStyle](./get_dashstyle/)() | Spécifie le motif point-tiret pour un trait. |
| [get_EndArrowLength](./get_endarrowlength/)() | Définit la longueur de la pointe de flèche pour l'extrémité d'un trait. |
| [get_EndArrowType](./get_endarrowtype/)() | Définit la pointe de flèche pour l'extrémité d'un trait. |
| [get_EndArrowWidth](./get_endarrowwidth/)() | Définit la largeur de la pointe de flèche pour l'extrémité d'un trait. |
| [get_EndCap](./get_endcap/)() | Définit le style de terminaison pour l'extrémité d'un trait. |
| [get_Fill](./get_fill/)() | Obtient le format de remplissage pour le [Stroke](./). |
| [get_ForeColor](./get_forecolor/)() | Obtient ou définit la couleur de premier plan du trait. |
| [get_ForeThemeColor](./get_forethemecolor/)() | Obtient ou définit un objet ThemeColor qui représente la couleur de premier plan du trait. |
| [get_ForeTintAndShade](./get_foretintandshade/)() | Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur de premier plan du trait. |
| [get_ImageBytes](./get_imagebytes/)() | Définit l'image pour un remplissage d'image ou de motif de trait. |
| [get_JoinStyle](./get_joinstyle/)() | Définit le style de jointure d'une polyligne. |
| [get_LineStyle](./get_linestyle/)() | Définit le style de ligne du trait. |
| [get_On](./get_on/)() | Définit si le chemin sera tracé. |
| [get_Opacity](./get_opacity/)() | Définit le degré de transparence d'un trait. La plage valide est de 0 à 1. |
| [get_StartArrowLength](./get_startarrowlength/)() | Définit la longueur de la pointe de flèche pour le début d'un trait. |
| [get_StartArrowType](./get_startarrowtype/)() | Définit la pointe de flèche pour le début d'un trait. |
| [get_StartArrowWidth](./get_startarrowwidth/)() | Définit la largeur de la pointe de flèche pour le début d'un trait. |
| [get_Transparency](./get_transparency/)() | Obtient ou définit une valeur entre 0.0 (opaque) et 1.0 (transparent) représentant le degré de transparence du trait. |
| [get_Visible](./get_visible/)() | Obtient ou définit un indicateur indiquant si le trait est visible. |
| [get_Weight](./get_weight/)() | Définit l'épaisseur du pinceau qui trace le chemin d'une forme en points. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Mutateur pour [Aspose::Words::Drawing::Stroke::get_BackColor](./get_backcolor/). |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | Mutateur pour [Aspose::Words::Drawing::Stroke::get_BackThemeColor](./get_backthemecolor/). |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | Mutateur pour [Aspose::Words::Drawing::Stroke::get_BackTintAndShade](./get_backtintandshade/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Mutateur pour [Aspose::Words::Drawing::Stroke::get_Color](./get_color/). |
| [set_Color2](./set_color2/)(System::Drawing::Color) | Mutateur pour [Aspose::Words::Drawing::Stroke::get_Color2](./get_color2/). |
| [set_DashStyle](./set_dashstyle/)(Aspose::Words::Drawing::DashStyle) | Spécifie le motif point-tiret pour un trait. |
| [set_EndArrowLength](./set_endarrowlength/)(Aspose::Words::Drawing::ArrowLength) | Définit la longueur de la pointe de flèche pour l'extrémité d'un trait. |
| [set_EndArrowType](./set_endarrowtype/)(Aspose::Words::Drawing::ArrowType) | Définit la pointe de flèche pour l'extrémité d'un trait. |
| [set_EndArrowWidth](./set_endarrowwidth/)(Aspose::Words::Drawing::ArrowWidth) | Définit la largeur de la pointe de flèche pour l'extrémité d'un trait. |
| [set_EndCap](./set_endcap/)(Aspose::Words::Drawing::EndCap) | Définit le style de terminaison pour l'extrémité d'un trait. |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | Mutateur pour [Aspose::Words::Drawing::Stroke::get_ForeColor](./get_forecolor/). |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | Mutateur pour [Aspose::Words::Drawing::Stroke::get_ForeThemeColor](./get_forethemecolor/). |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | Définisseur pour [Aspose::Words::Drawing::Stroke::get_ForeTintAndShade](./get_foretintandshade/). |
| [set_JoinStyle](./set_joinstyle/)(Aspose::Words::Drawing::JoinStyle) | Définisseur pour [Aspose::Words::Drawing::Stroke::get_JoinStyle](./get_joinstyle/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::Drawing::ShapeLineStyle) | Définisseur pour [Aspose::Words::Drawing::Stroke::get_LineStyle](./get_linestyle/). |
| [set_On](./set_on/)(bool) | Définisseur pour [Aspose::Words::Drawing::Stroke::get_On](./get_on/). |
| [set_Opacity](./set_opacity/)(double) | Définit le degré de transparence d'un trait. La plage valide est de 0 à 1. |
| [set_StartArrowLength](./set_startarrowlength/)(Aspose::Words::Drawing::ArrowLength) | Définit la longueur de la pointe de flèche pour le début d'un trait. |
| [set_StartArrowType](./set_startarrowtype/)(Aspose::Words::Drawing::ArrowType) | Définit la pointe de flèche pour le début d'un trait. |
| [set_StartArrowWidth](./set_startarrowwidth/)(Aspose::Words::Drawing::ArrowWidth) | Définit la largeur de la pointe de flèche pour le début d'un trait. |
| [set_Transparency](./set_transparency/)(double) | Définisseur pour [Aspose::Words::Drawing::Stroke::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | Définisseur pour [Aspose::Words::Drawing::Stroke::get_Visible](./get_visible/). |
| [set_Weight](./set_weight/)(double) | Définisseur pour [Aspose::Words::Drawing::Stroke::get_Weight](./get_weight/). |
| static [Type](./type/)() |  |
## Remarques


Utilisez la propriété [Stroke](../shape/get_stroke/) pour accéder aux propriétés de contour d'une forme. Vous ne créez pas d'instances de la classe [Stroke](./) directement.

## Exemples



Montre comment modifier les propriétés du trait.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// Les formes de base, comme le rectangle, ont deux parties visibles.
// 1 -  Le remplissage, qui s'applique à la zone à l'intérieur du contour de la forme :
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  Le trait, qui délimite le contour de la forme :
// Modifiez diverses propriétés du trait de cette forme.
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_On(true);
stroke->set_Weight(5);
stroke->set_Color(System::Drawing::Color::get_Red());
stroke->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDashDotDot);
stroke->set_JoinStyle(Aspose::Words::Drawing::JoinStyle::Miter);
stroke->set_EndCap(Aspose::Words::Drawing::EndCap::Square);
stroke->set_LineStyle(Aspose::Words::Drawing::ShapeLineStyle::Triple);
stroke->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Red(), System::Drawing::Color::get_Blue(), Aspose::Words::Drawing::GradientStyle::Vertical, Aspose::Words::Drawing::GradientVariant::Variant1);

doc->Save(get_ArtifactsDir() + u"Shape.Stroke.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
