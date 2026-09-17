---
title: "Méthode Aspose::Words::Loading::LoadOptions::get_TempFolder"
linktitle: "get_TempFolder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Loading::LoadOptions::get_TempFolder. Permet d'utiliser des fichiers temporaires lors de la lecture d'un document. Par défaut, cette propriété est null et aucun fichier temporaire n'est utilisé en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.loading/loadoptions/get_tempfolder/
---
## LoadOptions::get_TempFolder method


Permet d'utiliser des fichiers temporaires lors de la lecture du document. Par défaut, cette propriété est **null** et aucun fichier temporaire n'est utilisé.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_TempFolder() const
```

## Remarques


Le dossier doit exister et être accessible en écriture, sinon une exception sera levée.

Aspose.Words supprime automatiquement tous les fichiers temporaires lorsque la lecture est terminée.

## Exemples



Montre comment charger un document en utilisant des fichiers temporaires.
```cpp
// Notez que cette approche peut réduire l'utilisation de la mémoire mais ralentit la vitesse.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_TempFolder(u"C:\\TempFolder\\");

// Assurez-vous que le répertoire existe et chargez
System::IO::Directory::CreateDirectory_(loadOptions->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);
```


Montre comment utiliser le disque dur au lieu de la mémoire lors du chargement d'un document.
```cpp
// Lorsque nous chargeons un document, divers éléments sont temporairement stockés en mémoire pendant que l'opération d'enregistrement se produit.
// Nous pouvons utiliser cette option pour utiliser un dossier temporaire dans le système de fichiers local à la place,
// ce qui réduira la surcharge mémoire de notre application.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// Le dossier temporaire spécifié doit exister dans le système de fichiers local avant l'opération de chargement.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", options);

// Le dossier persistera sans aucun contenu résiduel provenant de l'opération de chargement.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Voir aussi

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
