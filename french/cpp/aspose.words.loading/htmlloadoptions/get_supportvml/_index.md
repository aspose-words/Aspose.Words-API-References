---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml méthode"
linktitle: "get_SupportVml"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml méthode. Obtient ou définit une valeur indiquant s'il faut prendre en charge les images VML en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.loading/htmlloadoptions/get_supportvml/
---
## HtmlLoadOptions::get_SupportVml method


Obtient ou définit une valeur indiquant s'il faut prendre en charge les images VML.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml() const
```


## Exemples



Montre comment prendre en charge les commentaires conditionnels lors du chargement d'un document HTML.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Si la valeur est vraie, alors nous prenons en compte le code VML lors de l'analyse du document chargé.
loadOptions->set_SupportVml(supportVml);

// Ce document contient une image JPEG dans les balises "<!--[if gte vml 1]>" ,
// et une image PNG différente dans les balises "<![if !vml]>".
// Si nous définissons le drapeau "SupportVml" sur "true", alors Aspose.Words chargera le JPEG.
// Si nous définissons ce drapeau sur "false", alors Aspose.Words ne chargera que le PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Voir aussi

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
