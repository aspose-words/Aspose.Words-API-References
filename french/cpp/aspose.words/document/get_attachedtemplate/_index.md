---
title: "Aspose::Words::Document::get_AttachedTemplate méthode"
linktitle: "get_AttachedTemplate"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_AttachedTemplate méthode. Obtient ou définit le chemin complet du modèle attaché au document en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words/document/get_attachedtemplate/
---
## Document::get_AttachedTemplate method


Obtient ou définit le chemin complet du modèle attaché au document.

```cpp
System::String Aspose::Words::Document::get_AttachedTemplate()
```

## Remarques


Une chaîne vide signifie que le document est attaché au modèle Normal.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
