---
title: "Aspose::Words::Drawing::ShadowFormat class"
linktitle: "ShadowFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShadowFormat class. Représente le format d'ombre pour un objet. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.drawing/shadowformat/
---
## ShadowFormat class


Représente le format d'ombre d'un objet. Pour en savoir plus, consultez l'article de documentation [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/) .

```cpp
class ShadowFormat : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clear](./clear/)() | Efface le format d'ombre. |
| [get_Color](./get_color/)() | Obtient ou définit un objet **Color** qui représente la couleur de l'ombre. La valeur par défaut est **Black**. |
| [get_Transparency](./get_transparency/)() | Obtient ou définit le degré de transparence de l'effet d'ombre comme une valeur comprise entre 0.0 (opaque) et 1.0 (transparent). La valeur par défaut est 0.0. |
| [get_Type](./get_type/)() | Obtient ou définit le [ShadowType](../shadowtype/) spécifié pour [ShadowFormat](./). |
| [get_Visible](./get_visible/)() | Renvoie **true** si le formatage appliqué à cette instance est visible. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Drawing::ShadowFormat::get_Color](./get_color/). |
| [set_Transparency](./set_transparency/)(double) | Définisseur pour [Aspose::Words::Drawing::ShadowFormat::get_Transparency](./get_transparency/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::ShadowType) | Définisseur pour [Aspose::Words::Drawing::ShadowFormat::get_Type](./get_type/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment obtenir la couleur de l'ombre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
