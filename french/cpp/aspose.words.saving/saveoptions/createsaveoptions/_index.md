---
title: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions méthode"
linktitle: "CreateSaveOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::SaveOptions::CreateSaveOptions. Crée un objet d'options d'enregistrement d'une classe adaptée au format d'enregistrement spécifié en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.saving/saveoptions/createsaveoptions/
---
## SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat) method


Crée un objet d'options d'enregistrement d'une classe adaptée au format d'enregistrement spécifié.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement pour lequel créer un objet d'options d'enregistrement. |

### ReturnValue

Un objet d'une classe qui dérive de [SaveOptions](../).

## Voir aussi

* Class [SaveOptions](../)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## SaveOptions::CreateSaveOptions(const System::String\&) method


Crée un objet d'options d'enregistrement d'une classe adaptée à l'extension de fichier spécifiée dans le nom de fichier fourni.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | L'extension de ce nom de fichier détermine la classe de l'objet d'options d'enregistrement à créer. |

### ReturnValue

Un objet d'une classe qui dérive de [SaveOptions](../).

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
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
