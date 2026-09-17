---
title: "Aspose::Words::Document::get_RemovePersonalInformation méthode"
linktitle: "get_RemovePersonalInformation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_RemovePersonalInformation méthode. Obtient ou définit un indicateur indiquant que Microsoft Word supprimera toutes les informations utilisateur des commentaires, des révisions et des propriétés du document lors de l'enregistrement du document en C++."
type: docs
weight: 45000
url: /fr/cpp/aspose.words/document/get_removepersonalinformation/
---
## Document::get_RemovePersonalInformation method


Obtient ou définit un indicateur indiquant que Microsoft Word supprimera toutes les informations utilisateur des commentaires, révisions et propriétés du document lors de l'enregistrement du document.

```cpp
bool Aspose::Words::Document::get_RemovePersonalInformation()
```


## Exemples



Montre comment activer la suppression des informations personnelles lors d'un enregistrement manuel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez du contenu contenant des informations personnelles.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
doc->get_BuiltInDocumentProperties()->set_Company(u"Placeholder Inc.");

doc->StartTrackRevisions(doc->get_BuiltInDocumentProperties()->get_Author(), System::DateTime::get_Now());
builder->Write(u"Hello world!");
doc->StopTrackRevisions();

// Cet indicateur est équivalent à Fichier -> Options -> Centre de confiance -> Paramètres du Centre de confiance... ->
// Options de confidentialité -> "Supprimer les informations personnelles des propriétés du fichier lors de l'enregistrement" dans Microsoft Word.
doc->set_RemovePersonalInformation(saveWithoutPersonalInfo);

// Cette option ne prendra pas effet lors d'une opération d'enregistrement effectuée avec Aspose.Words.
// Les données personnelles seront supprimées de notre document lorsque l'indicateur est activé lors d'un enregistrement manuel avec Microsoft Word.
doc->Save(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");

ASPOSE_ASSERT_EQ(saveWithoutPersonalInfo, doc->get_RemovePersonalInformation());
ASSERT_EQ(u"John Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Placeholder Inc.", doc->get_BuiltInDocumentProperties()->get_Company());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
