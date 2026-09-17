---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty méthode"
linktitle: "get_UpdateLastPrintedProperty"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty méthode. Obtient ou définit une valeur déterminant si la propriété LastPrinted est mise à jour avant l'enregistrement en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.saving/saveoptions/get_updatelastprintedproperty/
---
## SaveOptions::get_UpdateLastPrintedProperty method


Obtient ou définit une valeur déterminant si la propriété [LastPrinted](../../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) est mise à jour avant l'enregistrement.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty() const
```


## Exemples



Montre comment mettre à jour la propriété "Dernière impression" d'un document lors de l'enregistrement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime lastPrinted(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_LastPrinted(lastPrinted);

// Ce drapeau détermine si la date de la dernière impression, qui est une propriété intégrée, est mise à jour.
// Le cas échéant, la date de la dernière opération d'enregistrement du document
// avec cet objet SaveOptions passé en paramètre est utilisée comme date d'impression.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateLastPrintedProperty(isUpdateLastPrintedProperty);

// Dans Microsoft Word 2003, cette propriété est accessible via Fichier -> Propriétés -> Statistiques -> Imprimé.
// Elle peut également être affichée dans le corps du document en utilisant un champ PRINTDATE.
doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Ouvrez le document enregistré, puis vérifiez la valeur de la propriété.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
{
    ASSERT_NE(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
else
{
    ASSERT_EQ(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
```

## Voir aussi

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
