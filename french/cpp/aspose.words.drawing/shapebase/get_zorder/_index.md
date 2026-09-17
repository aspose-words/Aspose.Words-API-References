---
title: "Aspose::Words::Drawing::ShapeBase::get_ZOrder méthode"
linktitle: "get_ZOrder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_ZOrder méthode. Détermine l'ordre d'affichage des formes qui se chevauchent en C++."
type: docs
weight: 57000
url: /fr/cpp/aspose.words.drawing/shapebase/get_zorder/
---
## ShapeBase::get_ZOrder method


Détermine l'ordre d'affichage des formes qui se chevauchent.

```cpp
int32_t Aspose::Words::Drawing::ShapeBase::get_ZOrder()
```

## Remarques


N'a d'effet que pour les formes de niveau supérieur.

La valeur par défaut est 0.

Le nombre représente la priorité d'empilement. Une forme avec un nombre plus élevé sera affichée comme si elle chevauchait (en \"avant\" de) une forme avec un nombre plus bas.

L'ordre des formes qui se chevauchent est indépendant pour les formes dans l'en-tête et dans le texte principal du document.

L'ordre d'affichage des formes enfants dans une forme groupée est déterminé par leur ordre à l'intérieur de la forme groupée.

## Exemples



Montre comment manipuler l'ordre des formes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez trois rectangles de couleurs différentes qui se chevauchent partiellement.
// Lorsque nous insérons une forme qui chevauche une autre forme, Aspose.Words place la forme la plus récente au-dessus de l'ancienne.
// Le rectangle vert clair chevauchera le rectangle bleu clair et le masquera partiellement,
// et le rectangle bleu clair masquera le rectangle orange.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 150, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 150, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 200, 200, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_LightGreen());

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

// La propriété \"ZOrder\" d'une forme détermine sa priorité d'empilement parmi les autres formes qui se chevauchent.
// Si deux formes qui se chevauchent ont des valeurs \"ZOrder\" différentes,
// Microsoft Word placera la forme avec une valeur plus élevée au-dessus de la forme avec la valeur la plus basse.
// Définissez les valeurs \"ZOrder\" de nos formes pour placer le premier rectangle orange au-dessus du deuxième rectangle bleu clair
// et le deuxième rectangle bleu clair au-dessus du troisième rectangle vert clair.
// Cela inversera leur ordre d'empilement original.
shapes[0]->set_ZOrder(3);
shapes[1]->set_ZOrder(2);
shapes[2]->set_ZOrder(1);

doc->Save(get_ArtifactsDir() + u"Shape.ZOrder.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
