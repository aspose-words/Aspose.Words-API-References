---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty méthode"
linktitle: "get_UpdateLastSavedTimeProperty"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty méthode. Obtient ou définit une valeur déterminant si la propriété LastSavedTime est mise à jour avant l'enregistrement en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words.saving/saveoptions/get_updatelastsavedtimeproperty/
---
## SaveOptions::get_UpdateLastSavedTimeProperty method


Obtient ou définit une valeur déterminant si la propriété [LastSavedTime](../../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) est mise à jour avant l'enregistrement.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty() const
```


## Exemples



Montre comment déterminer s'il faut préserver la propriété "Last saved time" du document lors de l'enregistrement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), doc->get_BuiltInDocumentProperties()->get_LastSavedTime());

// Lorsque nous enregistrons le document au format OOXML, nous pouvons créer un objet OoxmlSaveOptions
// et le transmettre ensuite à la méthode d'enregistrement du document pour modifier la façon dont nous enregistrons le document.
// Définissez la propriété "UpdateLastSavedTimeProperty" sur "true" pour
// définir la propriété intégrée "Last saved time" du document de sortie à la date/heure actuelle.
// Définissez la propriété "UpdateLastSavedTimeProperty" sur "false" pour
// préserver la valeur originale de la propriété intégrée "Last saved time" du document d'entrée.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_UpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx");
System::DateTime lastSavedTimeNew = doc->get_BuiltInDocumentProperties()->get_LastSavedTime();

if (updateLastSavedTimeProperty)
{
    ASSERT_TRUE((System::DateTime::get_Now() - lastSavedTimeNew).get_Days() < 1);
}
else
{
    ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), lastSavedTimeNew);
}
```

## Voir aussi

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
