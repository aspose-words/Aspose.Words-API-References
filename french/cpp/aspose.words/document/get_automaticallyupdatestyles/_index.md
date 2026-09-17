---
title: "Méthode Aspose::Words::Document::get_AutomaticallyUpdateStyles"
linktitle: "get_AutomaticallyUpdateStyles"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::get_AutomaticallyUpdateStyles. Obtient ou définit un indicateur indiquant si les styles du document sont mis à jour pour correspondre aux styles du modèle attaché chaque fois que le document est ouvert dans MS Word en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words/document/get_automaticallyupdatestyles/
---
## Document::get_AutomaticallyUpdateStyles method


Obtient ou définit un indicateur indiquant si les styles du document sont mis à jour pour correspondre aux styles du modèle attaché chaque fois que le document est ouvert dans MS Word.

```cpp
bool Aspose::Words::Document::get_AutomaticallyUpdateStyles()
```


## Exemples



Montre comment attacher un modèle à un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Les documents Microsoft Word sont fournis par défaut avec un modèle attaché appelé \"Normal.dotm\".
// Il n'existe aucun modèle par défaut pour les documents Aspose.Words vierges.
ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Attachez un modèle, puis définissez l'indicateur pour appliquer les modifications de style
// dans le modèle aux styles de notre document.
doc->set_AttachedTemplate(get_MyDir() + u"Business brochure.dotx");
doc->set_AutomaticallyUpdateStyles(true);

doc->Save(get_ArtifactsDir() + u"Document.AutomaticallyUpdateStyles.docx");
```


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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
