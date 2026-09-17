---
title: "Méthode Aspose::Words::Saving::SaveOutputParameters::get_ContentType"
linktitle: "get_ContentType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::SaveOutputParameters::get_ContentType. Retourne la chaîne Content-Type (type de média Internet) qui identifie le type du document enregistré en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.saving/saveoutputparameters/get_contenttype/
---
## SaveOutputParameters::get_ContentType method


Renvoie la chaîne Content-Type (type de média Internet) qui identifie le type du document enregistré.

```cpp
System::String Aspose::Words::Saving::SaveOutputParameters::get_ContentType() const
```


## Exemples



Montre comment accéder aux paramètres de sortie d'une opération d'enregistrement de document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Après avoir enregistré un document, nous pouvons accéder au type de média Internet (type MIME) du nouveau document de sortie créé.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// Cette propriété change en fonction du format d'enregistrement.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## Voir aussi

* Class [SaveOutputParameters](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
