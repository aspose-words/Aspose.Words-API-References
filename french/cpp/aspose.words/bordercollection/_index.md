---
title: "Aspose::Words::BorderCollection classe"
linktitle: "BorderCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BorderCollection classe. Une collection d'objets Border. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/bordercollection/
---
## BorderCollection class


Une collection d'objets [Border](../border/). Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class BorderCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Border>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Supprime toutes les bordures d'un objet. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::BorderCollection\>\&) | Compare les collections de bordures. |
| [get_Bottom](./get_bottom/)() | Obtient la bordure inférieure. |
| [get_Color](./get_color/)() | Obtient ou définit la couleur de la bordure. |
| [get_Count](./get_count/)() | Obtient le nombre de bordures dans la collection. |
| [get_DistanceFromText](./get_distancefromtext/)() | Obtient ou définit la distance de la bordure par rapport au texte en points. |
| [get_Horizontal](./get_horizontal/)() | Obtient la bordure horizontale utilisée entre les cellules ou les paragraphes correspondants. |
| [get_Left](./get_left/)() | Obtient la bordure gauche. |
| [get_LineStyle](./get_linestyle/)() | Obtient ou définit le style de la bordure. |
| [get_LineWidth](./get_linewidth/)() | Obtient ou définit la largeur de la bordure en points. |
| [get_Right](./get_right/)() | Obtient la bordure droite. |
| [get_Shadow](./get_shadow/)() | Obtient ou définit une valeur indiquant si la bordure a une ombre. |
| [get_Top](./get_top/)() | Obtient la bordure supérieure. |
| [get_Vertical](./get_vertical/)() | Obtient la bordure verticale utilisée entre les cellules. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur qui peut être utilisé pour parcourir toutes les bordures de la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::BorderType) | Récupère un objet [Border](../border/) par type de bordure. |
| [idx_get](./idx_get/)(int32_t) | Récupère un objet [Border](../border/) par indice. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Mutateur pour [Aspose::Words::BorderCollection::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Mutateur pour [Aspose::Words::BorderCollection::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Mutateur pour [Aspose::Words::BorderCollection::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Mutateur pour [Aspose::Words::BorderCollection::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Définisseur de [Aspose::Words::BorderCollection::get_Shadow](./get_shadow/). |
| static [Type](./type/)() |  |

## Exemples



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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
