---
title: "Aspose::Words::Drawing::ShapeBase::get_AlternativeText méthode"
linktitle: "get_AlternativeText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AlternativeText méthode. Définit le texte alternatif à afficher à la place d'un graphique en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.drawing/shapebase/get_alternativetext/
---
## ShapeBase::get_AlternativeText method


Définit le texte alternatif à afficher à la place d'un graphique.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_AlternativeText()
```

## Remarques


La valeur par défaut est une chaîne vide.

## Exemples



Montre comment utiliser le texte alternatif d'une forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 150, 150);
shape->set_Name(u"MyCube");

shape->set_AlternativeText(u"Alt text for MyCube.");

// Nous pouvons accéder au texte alternatif d'une forme en cliquant dessus avec le bouton droit, puis via "Format AutoShape" → "Alt Text".
doc->Save(get_ArtifactsDir() + u"Shape.AltText.docx");

// Enregistrez le document au format HTML, puis supprimez l'image liée qui appartient à notre forme.
// Le navigateur qui lit notre HTML affichera le texte alt à la place de l'image manquante.
doc->Save(get_ArtifactsDir() + u"Shape.AltText.html");
System::IO::File::Delete(get_ArtifactsDir() + u"Shape.AltText.001.png");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
