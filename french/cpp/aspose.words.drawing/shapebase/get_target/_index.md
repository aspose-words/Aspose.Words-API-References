---
title: "Aspose::Words::Drawing::ShapeBase::get_Target method"
linktitle: "get_Target"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Target method. Obtient ou définit le cadre cible pour le lien hypertexte de la forme en C++."
type: docs
weight: 50000
url: /fr/cpp/aspose.words.drawing/shapebase/get_target/
---
## ShapeBase::get_Target method


Obtient ou définit le cadre cible pour le lien hypertexte de la forme.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Target()
```

## Remarques


La valeur par défaut est une chaîne vide.

## Exemples



Montre comment insérer une forme contenant une image et qui est également un hyperlien.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Ctrl + clic gauche sur la forme dans Microsoft Word ouvrira une nouvelle fenêtre de navigateur web
// et nous amènera à l'hyperlien dans la propriété \"HRef\".
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
