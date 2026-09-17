---
title: "Méthode Aspose::Words::Saving::SaveOptions::get_TempFolder"
linktitle: "get_TempFolder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::SaveOptions::get_TempFolder. Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement d'un fichier DOC ou DOCX. Par défaut, cette propriété est null et aucun fichier temporaire n'est utilisé en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.saving/saveoptions/get_tempfolder/
---
## SaveOptions::get_TempFolder method


Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement en fichier DOC ou DOCX. Par défaut, cette propriété est **null** et aucun fichier temporaire n'est utilisé.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_TempFolder() const
```

## Remarques


Lorsque Aspose.Words enregistre un document, il doit créer des structures internes temporaires. Par défaut, ces structures internes sont créées en mémoire et l'utilisation de la mémoire augmente brièvement pendant que le document est en cours d'enregistrement. Une fois l'enregistrement terminé, la mémoire est libérée et récupérée par le ramasse-miettes.

Spécifier un dossier temporaire à l'aide de [TempFolder](./) fera en sorte qu'Aspose.Words conserve les structures internes dans des fichiers temporaires plutôt qu'en mémoire. Cela réduit l'utilisation de la mémoire pendant l'enregistrement, mais diminuera les performances de sauvegarde.

Le dossier doit exister et être accessible en écriture, sinon une exception sera levée.

Aspose.Words supprime automatiquement tous les fichiers temporaires une fois l'enregistrement terminé.

## Exemples



Montre comment utiliser le disque dur au lieu de la mémoire lors de l'enregistrement d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Lorsque nous enregistrons un document, divers éléments sont temporairement stockés en mémoire pendant que l'opération d'enregistrement se déroule.
// Nous pouvons utiliser cette option pour utiliser un dossier temporaire dans le système de fichiers local à la place,
// ce qui réduira la surcharge mémoire de notre application.
auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// Le dossier temporaire spécifié doit exister dans le système de fichiers local avant l'opération d'enregistrement.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.TempFolder.doc", options);

// Le dossier persistera sans aucun contenu résiduel provenant de l'opération de chargement.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Voir aussi

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
