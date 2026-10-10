---
title: "classe Aspose::Words::Drawing::ReflectionFormat"
linktitle: "ReflectionFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Drawing::ReflectionFormat. Représente le format de réflexion pour un objet en C++."
type: docs
weight: 9500
url: /fr/cpp/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class


Représente le format de réflexion d'un objet.

```cpp
class ReflectionFormat : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Blur](./get_blur/)() | Obtient ou définit une valeur double qui spécifie le degré d'effet de flou appliqué à l'effet de réflexion en points. La valeur par défaut est 0,0. |
| [get_Distance](./get_distance/)() | Obtient ou définit une valeur double qui spécifie la quantité de séparation de l'image réfléchie par rapport à l'objet en points. La valeur par défaut est 0,0. |
| [get_Size](./get_size/)() | Obtient ou définit une valeur double entre 0,0 et 1,0 représentant la taille de la réflexion en pourcentage de l'objet reflété. La valeur par défaut est 0,0. |
| [get_Transparency](./get_transparency/)() | Obtient ou définit une valeur double entre 0,0 (opaque) et 1,0 (transparent) représentant le degré de transparence de l'effet de réflexion. La valeur par défaut est 0,0. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Supprime [ReflectionFormat](./) de l'objet parent. |
| [set_Blur](./set_blur/)(double) | Mutateur pour [Aspose::Words::Drawing::ReflectionFormat::get_Blur](./get_blur/). |
| [set_Distance](./set_distance/)(double) | Mutateur pour [Aspose::Words::Drawing::ReflectionFormat::get_Distance](./get_distance/). |
| [set_Size](./set_size/)(double) | Mutateur pour [Aspose::Words::Drawing::ReflectionFormat::get_Size](./get_size/). |
| [set_Transparency](./set_transparency/)(double) | Mutateur pour [Aspose::Words::Drawing::ReflectionFormat::get_Transparency](./get_transparency/). |
| static [Type](./type/)() |  |
## Remarques


Utilisez la propriété [Reflection](../shapebase/get_reflection/) pour accéder aux propriétés de réflexion d'un objet. Vous ne créez pas d'instances de la classe [ReflectionFormat](./) directement.

## Exemples



Montre comment interagir avec l'effet de forme de réflexion.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Reflection()->set_Transparency(0.37);
shape->get_Reflection()->set_Size(0.48);
shape->get_Reflection()->set_Blur(17.5);
shape->get_Reflection()->set_Distance(9.2);

doc->Save(get_ArtifactsDir() + u"Shape.Reflection.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Reflection.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::SharedPtr<Aspose::Words::Drawing::ReflectionFormat> reflectionFormat = shape->get_Reflection();

ASSERT_NEAR(0.37, reflectionFormat->get_Transparency(), 0.01);
ASSERT_NEAR(0.48, reflectionFormat->get_Size(), 0.01);
ASSERT_NEAR(17.5, reflectionFormat->get_Blur(), 0.01);
ASSERT_NEAR(9.2, reflectionFormat->get_Distance(), 0.01);

reflectionFormat->Remove();

ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Transparency());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Size());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Blur());
ASPOSE_ASSERT_EQ(0, reflectionFormat->get_Distance());
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
