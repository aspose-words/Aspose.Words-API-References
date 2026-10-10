---
title: "Méthode Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty"
linktitle: "get_UpdateCreatedTimeProperty"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty. Obtient ou définit une valeur déterminant si la propriété CreatedTime est mise à jour avant l'enregistrement. La valeur par défaut est false ; en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.saving/saveoptions/get_updatecreatedtimeproperty/
---
## SaveOptions::get_UpdateCreatedTimeProperty method


Obtient ou définit une valeur déterminant si la propriété [CreatedTime](../../../aspose.words.properties/builtindocumentproperties/get_createdtime/) est mise à jour avant l'enregistrement. La valeur par défaut est **false** ;.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty() const
```


## Exemples



Montre comment mettre à jour la propriété "CreatedTime" d'un document lors de l'enregistrement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime createdTime(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_CreatedTime(createdTime);

// Ce drapeau détermine si l'heure de création, qui est une propriété intégrée, est mise à jour.
// Le cas échéant, la date de la dernière opération d'enregistrement du document
// avec cet objet SaveOptions passé en paramètre est utilisé comme heure de création.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Ouvrez le document enregistré, puis vérifiez la valeur de la propriété.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
{
    ASSERT_NE(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
else
{
    ASSERT_EQ(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
```

## Voir aussi

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
