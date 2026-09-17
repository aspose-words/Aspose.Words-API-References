---
title: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked méthode"
linktitle: "get_AnchorLocked"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked méthode. Spécifie si l'ancre de la forme est verrouillée en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.drawing/shapebase/get_anchorlocked/
---
## ShapeBase::get_AnchorLocked method


Spécifie si l'ancre de la forme est verrouillée.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AnchorLocked()
```

## Remarques


La valeur par défaut est **false**.

N'a d'effet que pour les formes de niveau supérieur.

Cette propriété affecte le comportement de l'ancre de la forme dans Microsoft Word. Lorsque l'ancre n'est pas verrouillée, déplacer la forme dans Microsoft Word peut également déplacer l'ancre de la forme.

## Exemples



Montre comment verrouiller ou déverrouiller l'ancre de paragraphe d'une forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

builder->Write(u"Our shape will have an anchor attached to this paragraph.");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 160);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

builder->Writeln(u"Hello again!");

// Définissez la propriété "AnchorLocked" sur "true" pour empêcher l'ancre de la forme
// de se déplacer lors du déplacement de la forme dans Microsoft Word.
// Définissez la propriété "AnchorLocked" sur "false" pour autoriser tout déplacement de la forme
// pour également déplacer son ancre vers tout autre paragraphe auquel la forme se rapproche.
shape->set_AnchorLocked(anchorLocked);

// Si la forme n'a pas de symbole d'ancrage visible à sa gauche,
// nous devrons activer les ancres visibles via "Options" -> "Affichage" -> "Ancres d'objet".
doc->Save(get_ArtifactsDir() + u"Shape.AnchorLocked.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
