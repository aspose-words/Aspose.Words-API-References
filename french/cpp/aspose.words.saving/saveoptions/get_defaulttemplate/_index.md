---
title: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate méthode"
linktitle: "get_DefaultTemplate"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::SaveOptions::get_DefaultTemplate méthode. Obtient ou définit le chemin vers le modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est une chaîne vide en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/saveoptions/get_defaulttemplate/
---
## SaveOptions::get_DefaultTemplate method


Obtient ou définit le chemin vers le modèle par défaut (y compris le nom de fichier). La valeur par défaut pour cette propriété est **empty string**.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_DefaultTemplate() const
```


## Exemples



Montre comment définir un modèle par défaut pour les documents qui n'ont pas de modèles attachés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Active la mise à jour automatique des styles, mais n'attache pas de document modèle.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Puisqu'il n'existe aucun document modèle, le document n'avait nulle part où suivre les modifications de style.
// Utilisez un objet SaveOptions pour définir automatiquement un modèle
// si un document que nous enregistrons n'en possède pas.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## Voir aussi

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
