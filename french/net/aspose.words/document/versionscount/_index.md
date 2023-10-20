---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: Aspose.Words pour .NET
description: Document VersionsCount propriété. Obtient le nombre de versions de document stockées dans le document DOC en C#.
type: docs
weight: 460
url: /fr/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Obtient le nombre de versions de document stockées dans le document DOC.

```csharp
public int VersionsCount { get; }
```

## Remarques

Les versions dans Microsoft Word sont accessibles via le menu Fichier/Versions. Microsoft Word prend en charge les versions uniquement pour les fichiers DOC.

Cette propriété permet de détecter s'il y avait des versions de documents stockées dans ce document avant son ouverture dans Aspose.Words. Aspose.Words ne fournit aucune autre prise en charge pour les versions de document. Si vous enregistrez ce document à l'aide d'Aspose.Words, le document sera enregistré sans versions.

## Exemples

Montre comment utiliser la fonctionnalité de décompte des versions des anciens documents Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// On peut lire cette propriété d'un document, mais on ne peut pas la conserver lors de la sauvegarde.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");      
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
