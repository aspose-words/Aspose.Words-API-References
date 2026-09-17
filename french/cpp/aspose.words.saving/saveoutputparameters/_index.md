---
title: "Classe Aspose::Words::Saving::SaveOutputParameters"
linktitle: "SaveOutputParameters"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Saving::SaveOutputParameters. Cet objet est renvoyé à l'appelant après l'enregistrement d'un document et contient des informations supplémentaires qui ont été générées ou calculées pendant l'opération d'enregistrement. L'appelant peut utiliser ou ignorer cet objet. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class


Cet objet est renvoyé à l'appelant après l'enregistrement d'un document et contient des informations supplémentaires qui ont été générées ou calculées pendant l'opération d'enregistrement. L'appelant peut utiliser ou ignorer cet objet. Pour en savoir plus, consultez l'article de documentation [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class SaveOutputParameters : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_ContentType](./get_contenttype/)() const | Renvoie la chaîne Content-Type (type de média Internet) qui identifie le type du document enregistré. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
