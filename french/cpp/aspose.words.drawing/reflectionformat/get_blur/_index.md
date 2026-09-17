---
title: "Aspose::Words::Drawing::ReflectionFormat::get_Blur méthode"
linktitle: "get_Blur"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::ReflectionFormat::get_Blur. Obtient ou définit une valeur double qui spécifie le degré d'effet de flou appliqué à l'effet de réflexion en points. La valeur par défaut est 0.0 en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing/reflectionformat/get_blur/
---
## ReflectionFormat::get_Blur method


Obtient ou définit une valeur double qui spécifie le degré d'effet de flou appliqué à l'effet de réflexion en points. La valeur par défaut est 0,0.

```cpp
double Aspose::Words::Drawing::ReflectionFormat::get_Blur()
```


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

* Class [ReflectionFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
