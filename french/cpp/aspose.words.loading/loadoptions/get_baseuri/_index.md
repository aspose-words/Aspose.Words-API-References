---
title: "Aspose::Words::Loading::LoadOptions::get_BaseUri méthode"
linktitle: "get_BaseUri"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::LoadOptions::get_BaseUri méthode. Obtient ou définit la chaîne qui sera utilisée pour résoudre les URI relatifs trouvés dans le document en URI absolus lorsque nécessaire. Peut être nul ou une chaîne vide. La valeur par défaut est null en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.loading/loadoptions/get_baseuri/
---
## LoadOptions::get_BaseUri method


Obtient ou définit la chaîne qui sera utilisée pour résoudre les URI relatives trouvées dans le document en URI absolues lorsque cela est nécessaire. Peut être **null** ou une chaîne vide. La valeur par défaut est **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_BaseUri() const
```

## Remarques


Cette propriété est utilisée pour résoudre les URI relatifs en absolus dans les cas suivants :

1. Lors du chargement d'un document HTML depuis un flux et que le document contient des images avec des URI relatifs et n'a pas d'URI de base spécifié dans l'élément BASE du HTML.
1. Lors de l'enregistrement d'un document au format PDF et autres formats, pour récupérer les images liées à l'aide d'URI relatifs afin que les images puissent être enregistrées dans le document de sortie.



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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
