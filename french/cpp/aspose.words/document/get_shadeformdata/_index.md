---
title: "Aspose::Words::Document::get_ShadeFormData méthode"
linktitle: "get_ShadeFormData"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_ShadeFormData méthode. Indique s'il faut activer l'ombrage gris sur les champs de formulaire en C++."
type: docs
weight: 49000
url: /fr/cpp/aspose.words/document/get_shadeformdata/
---
## Document::get_ShadeFormData method


Spécifie s'il faut activer l'ombrage gris sur les champs de formulaire.

```cpp
bool Aspose::Words::Document::get_ShadeFormData()
```


## Exemples



Montre comment appliquer un ombrage gris aux champs de formulaire.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world! ");
builder->InsertTextInput(u"My form field", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Text contents of form field, which are shaded in grey by default.", 0);

// Nous pouvons désactiver l'ombrage gris, afin que le texte marqué se fonde avec le reste du texte.
doc->set_ShadeFormData(useGreyShading);
doc->Save(get_ArtifactsDir() + u"Document.ShadeFormData.docx");
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
