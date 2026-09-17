---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInline méthode"
linktitle: "get_IsInline"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInline méthode. Un moyen rapide de déterminer si cette forme est positionnée en ligne avec le texte en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words.drawing/shapebase/get_isinline/
---
## ShapeBase::get_IsInline method


Un moyen rapide de déterminer si cette forme est positionnée en ligne avec le texte.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInline()
```

## Remarques


N'a d'effet que pour les formes de niveau supérieur.

## Exemples



Montre comment déterminer si une forme est en ligne ou flottante.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici deux types d'habillage que les formes peuvent avoir.
// 1 -  En ligne :
builder->Write(u"Hello world! ");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());
builder->Write(u" Hello again.");

// Une forme en ligne se trouve à l'intérieur d'un paragraphe parmi d'autres éléments de paragraphe, tels que des fragments de texte.
// Dans Microsoft Word, nous pouvons cliquer et faire glisser la forme vers n'importe quel paragraphe comme s'il s'agissait d'un caractère.
// Si la forme est grande, elle affectera l'espacement vertical des paragraphes.
// Nous ne pouvons pas déplacer cette forme vers un endroit sans paragraphe.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::Inline, shape->get_WrapType());
ASSERT_TRUE(shape->get_IsInline());

// 2 -  Flottant:
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

// Une forme flottante appartient au paragraphe dans lequel nous l'insérons,
// que nous pouvons déterminer par un symbole d'ancrage qui apparaît lorsque nous cliquons sur la forme.
// Si la forme n'a pas de symbole d'ancrage visible à sa gauche,
// nous devrons activer les ancres visibles via "Options" -> "Affichage" -> "Ancres d'objet".
// Dans Microsoft Word, nous pouvons cliquer avec le bouton gauche et faire glisser cette forme librement vers n'importe quel emplacement.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, shape->get_WrapType());
ASSERT_FALSE(shape->get_IsInline());

doc->Save(get_ArtifactsDir() + u"Shape.IsInline.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
