---
title: LoadOptions.TempFolder
second_title: Référence de l'API Aspose.Words pour .NET
description: LoadOptions propriété. Permet dutiliser des fichiers temporaires lors de la lecture dun document. Par défaut cette propriété estnul et aucun fichier temporaire nest utilisé.
type: docs
weight: 150
url: /fr/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Permet d'utiliser des fichiers temporaires lors de la lecture d'un document. Par défaut cette propriété est`nul` et aucun fichier temporaire n'est utilisé.

```csharp
public string TempFolder { get; set; }
```

### Remarques

Le dossier doit exister et être accessible en écriture, sinon une exception sera levée.

Aspose.Words supprime automatiquement tous les fichiers temporaires une fois la lecture terminée.

### Exemples

Montre comment charger un document à l'aide de fichiers temporaires.

```csharp
// Notez qu'une telle approche peut réduire l'utilisation de la mémoire mais dégrade la vitesse
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// S'assure que le répertoire existe et charge
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Montre comment utiliser le disque dur au lieu de la mémoire lors du chargement d'un document.

```csharp
// Lorsque nous chargeons un document, divers éléments sont temporairement stockés en mémoire au fur et à mesure de l'opération de sauvegarde.
// Nous pouvons utiliser cette option pour utiliser à la place un dossier temporaire dans le système de fichiers local,
// ce qui réduira la surcharge mémoire de notre application.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Le dossier temporaire spécifié doit exister dans le système de fichiers local avant l'opération de chargement.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// Le dossier persistera sans contenu résiduel de l'opération de chargement.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../loadoptions/)
* Assemblée [Aspose.Words](../../../)


