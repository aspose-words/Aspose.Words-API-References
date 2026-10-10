---
title: "Méthode Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell"
linktitle: "get_IsLayoutInCell"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell. Obtient ou définit un indicateur indiquant si la forme est affichée à l'intérieur d'un tableau ou à l'extérieur de celui-ci en C++."
type: docs
weight: 32000
url: /fr/cpp/aspose.words.drawing/shapebase/get_islayoutincell/
---
## ShapeBase::get_IsLayoutInCell method


Obtient ou définit un drapeau indiquant si la forme est affichée à l'intérieur d'un tableau ou en dehors de celui-ci.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell()
```

## Remarques


La valeur par défaut est **true**.

N'a d'effet que pour les formes de niveau supérieur, la propriété [WrapType](../get_wraptype/) dont la valeur est définie sur autre chose que [Inline](../../../aspose.words/inline/).

## Exemples



Montre comment déterminer comment afficher une forme dans une cellule de tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(10);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table->set_Style(tableStyle);

builder->MoveTo(table->get_FirstRow()->get_FirstCell()->get_FirstParagraph());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);

// Définissez la propriété "IsLayoutInCell" sur "true" pour afficher la forme comme un élément en ligne à l'intérieur du paragraphe de la cellule.
// L'origine des coordonnées qui déterminera l'emplacement de la forme sera le coin supérieur gauche de la cellule de la forme.
// Si nous redimensionnons la cellule, la forme se déplacera pour conserver la même position en partant du coin supérieur gauche de la cellule.
// Définissez la propriété "IsLayoutInCell" sur "false" pour afficher la forme comme une forme flottante indépendante.
// L'origine des coordonnées qui déterminera l'emplacement de la forme sera le coin supérieur gauche de la page,
// et la forme ne répondra à aucun redimensionnement de sa cellule.
shape->set_IsLayoutInCell(isLayoutInCell);

// Nous ne pouvons appliquer la propriété "IsLayoutInCell" qu'aux formes flottantes.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

doc->Save(get_ArtifactsDir() + u"Shape.LayoutInTableCell.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
