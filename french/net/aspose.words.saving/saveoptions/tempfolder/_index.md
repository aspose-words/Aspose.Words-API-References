---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words pour .NET
description: Optimisez l'enregistrement de vos documents avec la propriété SaveOptions TempFolder, qui désigne un dossier pour les fichiers DOC et DOCX temporaires, améliorant ainsi l'efficacité.
type: docs
weight: 140
url: /fr/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé.

```csharp
public string TempFolder { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| OutOfMemoryException | Lancez cette exception si vous enregistrez un document très volumineux (des milliers de pages) et/ou traitez de nombreux documents en même temps. Le pic de mémoire pendant l'enregistrement peut être suffisamment important pour provoquer l'exception. |

## Remarques

Lorsqu'Aspose.Words enregistre un document, il doit créer des structures internes temporaires. Par défaut, ces structures internes sont créées en mémoire et l'utilisation de la mémoire augmente brièvement pendant l'enregistrement du document. Une fois l'enregistrement terminé, la mémoire est libérée et récupérée par le ramasse-miettes.

Spécification d'un dossier temporaire à l'aide de`TempFolder` oblige Aspose.Words à conserver les structures internes dans des fichiers temporaires au lieu de les stocker en mémoire. Cela réduit l'utilisation de la mémoire lors de la sauvegarde, mais diminue les performances.

Le dossier doit exister et être accessible en écriture, sinon une exception sera levée.

Aspose.Words supprime automatiquement tous les fichiers temporaires une fois l'enregistrement terminé.

## Exemples

Montre comment utiliser le disque dur au lieu de la mémoire lors de l'enregistrement d'un document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Lorsque nous enregistrons un document, divers éléments sont temporairement stockés en mémoire pendant que l'opération de sauvegarde est en cours.
// Nous pouvons utiliser cette option pour utiliser un dossier temporaire dans le système de fichiers local à la place,
// ce qui réduira la surcharge de mémoire de notre application.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Le dossier temporaire spécifié doit exister dans le système de fichiers local avant l'opération de sauvegarde.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// Le dossier persistera sans aucun contenu résiduel de l'opération de chargement.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
