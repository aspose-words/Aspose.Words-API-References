---
title: "Aspose::Words::Border classe"
linktitle: "Border"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Border classe. Représente une bordure d'un objet. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/border/
---
## Border class


Représente une bordure d'un objet. Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Border : public Aspose::Words::InternableComplexAttr,
               public Aspose::Words::IComplexAttr
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Réinitialise les propriétés de la bordure aux valeurs par défaut. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Border\>\&) | Détermine si la bordure spécifiée est égale en valeur à la bordure actuelle. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [get_Color](./get_color/)() | Obtient ou définit la couleur de la bordure. |
| [get_DistanceFromText](./get_distancefromtext/)() | Obtient ou définit la distance de la bordure par rapport au texte ou au bord de la page en points. |
| [get_IsVisible](./get_isvisible/)() | Renvoie **true** si le [LineStyle](./get_linestyle/) n'est pas [None](../linestyle/). |
| [get_LineStyle](./get_linestyle/)() | Obtient ou définit le style de la bordure. |
| [get_LineWidth](./get_linewidth/)() | Obtient ou définit la largeur de la bordure en points. |
| [get_Shadow](./get_shadow/)() | Obtient ou définit une valeur indiquant si la bordure a une ombre. |
| [get_ThemeColor](./get_themecolor/)() | Obtient ou définit la couleur du thème dans le schéma de couleurs appliqué qui est associé à cet objet [Border](./). |
| [get_TintAndShade](./get_tintandshade/)() | Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur. |
| [GetHashCode](./gethashcode/)() const override | Servit de fonction de hachage pour ce type. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Border::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Définisseur pour [Aspose::Words::Border::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Définisseur pour [Aspose::Words::Border::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Définisseur pour [Aspose::Words::Border::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Définisseur pour [Aspose::Words::Border::get_Shadow](./get_shadow/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Méthode d'assignation pour [Aspose::Words::Border::get_ThemeColor](./get_themecolor/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Méthode d'assignation pour [Aspose::Words::Border::get_TintAndShade](./get_tintandshade/). |
| static [Type](./type/)() |  |
## Remarques


Les bordures peuvent être appliquées à divers éléments du document, y compris le paragraphe, le segment de texte à l'intérieur d'un paragraphe ou une cellule de tableau.

## Exemples



Montre comment insérer une chaîne entourée d'une bordure dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


Montre comment insérer un paragraphe avec une bordure supérieure.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Définissez ThemeColor uniquement lorsque LineWidth ou LineStyle sont définis.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Voir aussi

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
