---
title: "méthode Aspose::Words::Drawing::ShapeBase::get_Name"
linktitle: "get_Name"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "méthode Aspose::Words::Drawing::ShapeBase::get_Name. Obtient ou définit le nom optionnel de la forme en C++."
type: docs
weight: 40000
url: /fr/cpp/aspose.words.drawing/shapebase/get_name/
---
## ShapeBase::get_Name method


Obtient ou définit le nom optionnel de la forme.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Name()
```

## Remarques


La valeur par défaut est une chaîne vide.

Ne peut pas être **null**, mais peut être une chaîne vide.

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
