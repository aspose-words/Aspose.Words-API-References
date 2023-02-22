---
title: SaveOptions.TempFolder
second_title: Référence de l'API Aspose.Words pour .NET
description: SaveOptions propriété. Spécifie le dossier des fichiers temporaires utilisés lors de lenregistrement dans un fichier DOC ou DOCX. Par défaut cette propriété estnul et aucun fichier temporaire nest utilisé.
type: docs
weight: 150
url: /fr/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Spécifie le dossier des fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé.

```csharp
public string TempFolder { get; set; }
```

### Remarques

Lorsque Aspose.Words enregistre un document, il doit créer des structures internes temporaires. Par défaut, ces structures internes sont créées en mémoire et les pics d'utilisation de la mémoire pendant une courte période pendant le document est en cours d'enregistrement. Lorsque l'enregistrement est terminé, la mémoire est libérée et récupérée par le ramasse-miettes.

Si vous enregistrez un document très volumineux (des milliers de pages) et/ou traitez de nombreux documents en même temps, , le pic de mémoire lors de l'enregistrement peut être suffisamment important pour que le système lanceOutOfMemoryException . Spécification d'un dossier temporaire à l'aide`TempFolder` entraînera Aspose.Words à conserver les structures internes dans les fichiers temporaires au lieu de la mémoire. Cela réduit l'utilisation de la mémoire pendant l'enregistrement, mais diminue les performances d'enregistrement.

Le dossier doit exister et être accessible en écriture, sinon une exception sera levée.

Aspose.Words supprime automatiquement tous les fichiers temporaires lorsque l'enregistrement est terminé.

### Exemples

Montre comment utiliser le disque dur au lieu de la mémoire lors de l'enregistrement d'un document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Lorsque nous enregistrons un document, divers éléments sont temporairement stockés en mémoire au fur et à mesure de l'opération d'enregistrement.
// Nous pouvons utiliser cette option pour utiliser un dossier temporaire dans le système de fichiers local à la place,
// ce qui réduira la surcharge de mémoire de notre application.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Le dossier temporaire spécifié doit exister dans le système de fichiers local avant l'opération de sauvegarde.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// Le dossier persistera sans contenu résiduel de l'opération de chargement.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../saveoptions/)
* Assemblée [Aspose.Words](../../../)


