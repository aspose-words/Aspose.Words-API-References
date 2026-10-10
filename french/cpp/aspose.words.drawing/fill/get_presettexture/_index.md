---
title: "Aspose::Words::Drawing::Fill::get_PresetTexture méthode"
linktitle: "get_PresetTexture"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Fill::get_PresetTexture méthode. Obtient un PresetTexture pour le remplissage en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.drawing/fill/get_presettexture/
---
## Fill::get_PresetTexture method


Obtient un [PresetTexture](../../presettexture/) pour le remplissage.

```cpp
Aspose::Words::Drawing::PresetTexture Aspose::Words::Drawing::Fill::get_PresetTexture()
```


## Exemples



Montre comment remplir et carreler la texture à l'intérieur de la forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);

// Appliquer l'alignement de texture au remplissage de la forme.
shape->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(Aspose::Words::Drawing::TextureAlignment::TopRight);

// Utilisez l'option de conformité pour définir la forme en utilisant DML si vous souhaitez obtenir "TextureAlignment"
// propriété après l'enregistrement du document.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.TextureFill.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.TextureFill.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(Aspose::Words::Drawing::TextureAlignment::TopRight, shape->get_Fill()->get_TextureAlignment());
ASSERT_EQ(Aspose::Words::Drawing::PresetTexture::Canvas, shape->get_Fill()->get_PresetTexture());
```

## Voir aussi

* Enum [PresetTexture](../../presettexture/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
