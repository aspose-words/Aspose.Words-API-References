---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words pour .NET
description: SaveOptions TempFolder propriété. Spécifie le dossier des fichiers temporaires utilisé lors de lenregistrement dans un fichier DOC ou DOCX. Par défaut cette propriété estnul et aucun fichier temporaire nest utilisé en C#.
type: docs
weight: 140
url: /fr/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Spécifie le dossier des fichiers temporaires utilisé lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé.

```csharp
public string TempFolder { get; set; }
```

## Remarques

Lorsqu'Aspose.Words enregistre un document, il doit créer des structures internes temporaires. Par défaut, ces structures internes sont créées en mémoire et l'utilisation de la mémoire augmente pendant une courte période pendant que le document est en cours d'enregistrement. Une fois la sauvegarde terminée, la mémoire est libérée et récupérée par le garbage collector.

Si vous enregistrez un document très volumineux (des milliers de pages) et/ou traitez plusieurs documents en même temps, alors le pic de mémoire lors de l'enregistrement peut être suffisamment important pour que le système lanceOutOfMemoryException . Spécification d'un dossier temporaire à l'aide de`TempFolder` Aspose.Words conservera les structures internes dans les fichiers temporaires au lieu de la mémoire. Cela réduit l'utilisation de la mémoire pendant la sauvegarde, mais diminuera les performances de sauvegarde.

Le dossier doit exister et être accessible en écriture, sinon une exception sera levée.

Aspose.Words supprime automatiquement tous les fichiers temporaires une fois l'enregistrement terminé.

## Exemples

Montre comment utiliser le disque dur au lieu de la mémoire lors de l'enregistrement d'un document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Lorsque nous enregistrons un document, divers éléments sont temporairement stockés en mémoire pendant l'opération de sauvegarde.
// Nous pouvons utiliser cette option pour utiliser à la place un dossier temporaire dans le système de fichiers local,
// ce qui réduira la surcharge mémoire de notre application.
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
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
