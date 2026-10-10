---
title: "Aspose::Words::Drawing::ShapeBase::get_IsImage méthode"
linktitle: "get_IsImage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsImage méthode. Retourne true si cette forme est une forme image en C++."
type: docs
weight: 29000
url: /fr/cpp/aspose.words.drawing/shapebase/get_isimage/
---
## ShapeBase::get_IsImage method


Renvoie **true** si cette forme est une forme d'image.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsImage()
```


## Exemples



Montre comment ouvrir un document HTML avec des images depuis un flux en utilisant une URI de base.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Passez l'URI du dossier de base lors du chargement.
    // afin que toutes les images avec des URI relatifs dans le document HTML puissent être trouvées.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Vérifiez que la première forme du document contient une image valide.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
