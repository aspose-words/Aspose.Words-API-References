---
title: TempFolder
second_title: Référence de l'API Aspose.Words pour .NET
description: Permet dutiliser des fichiers temporaires lors de la lecture du document. Par défaut cette propriété estnul et aucun fichier temporaire nest utilisé.
type: docs
weight: 150
url: /fr/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Permet d'utiliser des fichiers temporaires lors de la lecture du document. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé.

```csharp
public string TempFolder { get; set; }
```

### Remarques

Le dossier doit exister et être accessible en écriture, sinon une exception sera levée.

Aspose.Words supprime automatiquement tous les fichiers temporaires lorsque la lecture est terminée.

### Exemples

Montre comment charger un document à l'aide de fichiers temporaires.

```csharp
// Notez qu'une telle approche peut réduire l'utilisation de la mémoire mais dégrade la vitesse
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Assurez-vous que le répertoire existe et chargez
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Montre comment utiliser le disque dur au lieu de la mémoire lors du chargement d'un document.

```csharp
// Lorsque nous chargeons un document, divers éléments sont temporairement stockés en mémoire au fur et à mesure de l'opération de sauvegarde.
// Nous pouvons utiliser cette option pour utiliser un dossier temporaire dans le système de fichiers local à la place,
// ce qui réduira la surcharge de mémoire de notre application.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Le dossier temporaire spécifié doit exister dans le système de fichiers local avant l'opération de chargement.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// Le dossier persistera sans contenu résiduel de l'opération de chargement.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Voir également

* class [LoadOptions](../../loadoptions)
* espace de noms [Aspose.Words.Loading](../../loadoptions)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->