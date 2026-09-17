---
title: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer méthode"
linktitle: "GetShapeRenderer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::GetShapeRenderer méthode. Crée et renvoie un objet qui peut être utilisé pour rendre cette forme dans une image en C++."
type: docs
weight: 58000
url: /fr/cpp/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase::GetShapeRenderer method


Crée et renvoie un objet pouvant être utilisé pour rendre cette forme en image.

```cpp
System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> Aspose::Words::Drawing::ShapeBase::GetShapeRenderer()
```


### ReturnValue

L'objet de rendu pour cette forme.
## Remarques


Cette méthode invoque simplement le constructeur [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/) et passe cet objet comme paramètre.

## Exemples



Montre comment utiliser un rendu de forme pour exporter des formes vers des fichiers dans le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// Il y a 7 formes dans le document, dont une forme groupée avec 2 formes enfants.
// Nous rendrons chaque forme dans un fichier image dans le système de fichiers local
// tout en ignorant les formes de groupe puisqu'elles n'ont aucune apparence.
// Cela produira 6 fichiers image.
for (auto&& shape : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    System::SharedPtr<Aspose::Words::Rendering::ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
    renderer->Save(get_ArtifactsDir() + System::String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## Voir aussi

* Class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
