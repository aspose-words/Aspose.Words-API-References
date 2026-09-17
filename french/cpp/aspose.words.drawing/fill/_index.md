---
title: "Aspose::Words::Drawing::Fill class"
linktitle: "Fill"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Drawing::Fill. Représente le format de remplissage d'un objet. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.drawing/fill/
---
## Fill class


Représente le format de remplissage d'un objet. Pour en savoir plus, consultez l'article de documentation [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class Fill : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Obtient ou définit un objet Color qui représente la couleur d'arrière-plan du remplissage. |
| [get_BackThemeColor](./get_backthemecolor/)() | Obtient ou définit un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage. |
| [get_BackTintAndShade](./get_backtintandshade/)() | Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan. |
| [get_BaseForeColor](./get_baseforecolor/)() | Obtient un objet Color qui représente la couleur de premier plan de base du remplissage sans aucun modificateur. |
| [get_Color](./get_color/)() | Obtient ou définit un objet Color qui représente la couleur de premier plan du remplissage. |
| [get_FillType](./get_filltype/)() | Obtient le type de remplissage. |
| [get_ForeColor](./get_forecolor/)() | Obtient un objet Color qui représente la couleur de premier plan du remplissage. |
| [get_ForeThemeColor](./get_forethemecolor/)() | Obtient ou définit un objet ThemeColor qui représente la couleur de premier plan du remplissage. |
| [get_ForeTintAndShade](./get_foretintandshade/)() | Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur de premier plan. |
| [get_GradientAngle](./get_gradientangle/)() | Obtient ou définit l'angle du remplissage en dégradé. |
| [get_GradientStops](./get_gradientstops/)() | Obtient une collection d'objets [GradientStop](../gradientstop/) pour le remplissage. |
| [get_GradientStyle](./get_gradientstyle/)() | Obtient le style de dégradé [GradientStyle](../gradientstyle/) pour le remplissage. |
| [get_GradientVariant](./get_gradientvariant/)() | Obtient la variante de dégradé [GradientVariant](../gradientvariant/) pour le remplissage. |
| [get_ImageBytes](./get_imagebytes/)() | Obtient les octets bruts de la texture ou du motif du remplissage. |
| [get_Opacity](./get_opacity/)() | Obtient ou définit le degré d'opacité du remplissage spécifié comme une valeur comprise entre 0.0 (transparent) et 1.0 (opaque). |
| [get_Pattern](./get_pattern/)() | Obtient un [PatternType](../patterntype/) pour le remplissage. |
| [get_PresetTexture](./get_presettexture/)() | Obtient une [PresetTexture](../presettexture/) pour le remplissage. |
| [get_RotateWithObject](./get_rotatewithobject/)() | Obtient si le remplissage tourne avec l'objet spécifié. |
| [get_TextureAlignment](./get_texturealignment/)() | Obtient ou définit l'alignement du remplissage de texture en mosaïque. |
| [get_Transparency](./get_transparency/)() | Obtient ou définit le degré de transparence du remplissage spécifié comme une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). |
| [get_Visible](./get_visible/)() | Obtient la valeur qui est **true** si le formatage appliqué à cette instance est visible. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OneColorGradient](./onecolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Définit le remplissage spécifié à un dégradé d'une seule couleur. |
| [OneColorGradient](./onecolorgradient/)(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Définit le remplissage spécifié à un dégradé d'une seule couleur en utilisant la couleur spécifiée. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType) | Définit le remplissage spécifié à un motif. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) | Définit le remplissage spécifié à un motif. |
| [PresetTextured](./presettextured/)(Aspose::Words::Drawing::PresetTexture) | Définit le remplissage avec une texture prédéfinie. |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Drawing::Fill::get_BackColor](./get_backcolor/). |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | Définisseur pour [Aspose::Words::Drawing::Fill::get_BackThemeColor](./get_backthemecolor/). |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | Définisseur pour [Aspose::Words::Drawing::Fill::get_BackTintAndShade](./get_backtintandshade/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Drawing::Fill::get_Color](./get_color/). |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | Définit un objet Color qui représente la couleur de premier plan du remplissage. |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | Définisseur pour [Aspose::Words::Drawing::Fill::get_ForeThemeColor](./get_forethemecolor/). |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | Définisseur pour [Aspose::Words::Drawing::Fill::get_ForeTintAndShade](./get_foretintandshade/). |
| [set_GradientAngle](./set_gradientangle/)(double) | Définisseur pour [Aspose::Words::Drawing::Fill::get_GradientAngle](./get_gradientangle/). |
| [set_Opacity](./set_opacity/)(double) | Définisseur pour [Aspose::Words::Drawing::Fill::get_Opacity](./get_opacity/). |
| [set_RotateWithObject](./set_rotatewithobject/)(bool) | Définit si le remplissage tourne avec l'objet spécifié. |
| [set_TextureAlignment](./set_texturealignment/)(Aspose::Words::Drawing::TextureAlignment) | Définisseur pour [Aspose::Words::Drawing::Fill::get_TextureAlignment](./get_texturealignment/). |
| [set_Transparency](./set_transparency/)(double) | Définisseur pour [Aspose::Words::Drawing::Fill::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | Définit la valeur qui est **true** si le formatage appliqué à cette instance est visible. |
| [SetImage](./setimage/)(const System::String\&) | Modifie le type de remplissage en image unique. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Modifie le type de remplissage en image unique. |
| [SetImage](./setimage/)(const System::ArrayPtr\<uint8_t\>\&) | Modifie le type de remplissage en image unique. |
| [Solid](./solid/)() | Définit le remplissage avec une couleur uniforme. |
| [Solid](./solid/)(System::Drawing::Color) | Définit le remplissage avec une couleur uniforme spécifiée. |
| [TwoColorGradient](./twocolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Définit le remplissage spécifié avec un dégradé à deux couleurs. |
| [TwoColorGradient](./twocolorgradient/)(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Définit le remplissage spécifié avec un dégradé à deux couleurs. |
| static [Type](./type/)() |  |
## Remarques


Utilisez la propriété [Fill](../shapebase/get_fill/) ou [Fill](../../aspose.words/font/get_fill/) pour accéder aux propriétés de remplissage d'un objet. Vous ne créez pas d'instances de la classe [Fill](./) directement.

## Exemples



Montre comment remplir une forme avec une couleur unie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Écrivez du texte, puis recouvrez-le d'une forme flottante.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Utilisez la propriété "StrokeColor" pour définir la couleur du contour de la forme.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Utilisez la propriété "FillColor" pour définir la couleur de la zone intérieure de la forme.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// La propriété "Opacity" détermine la transparence de la couleur sur une échelle de 0 à 1,
// 1 étant totalement opaque, et 0 étant invisible.
// Le remplissage de la forme est, par défaut, totalement opaque, donc nous ne pouvons pas voir le texte sur lequel cette forme se trouve.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Réglez l'opacité de la couleur de remplissage de la forme à une valeur plus basse afin que nous puissions voir le texte en dessous.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
