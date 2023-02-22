---
title: Document.VersionsCount
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Obtient le nombre de versions de document stockées dans le document DOC.
type: docs
weight: 440
url: /fr/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Obtient le nombre de versions de document stockées dans le document DOC.

```csharp
public int VersionsCount { get; }
```

### Remarques

Les versions dans Microsoft Word sont accessibles via le menu Fichier/Versions. Microsoft Word prend en charge les versions uniquement pour les fichiers DOC.

Cette propriété permet de détecter s'il y avait des versions de document stockées dans ce document avant son ouverture dans Aspose.Words. Aspose.Words ne fournit aucun autre support pour les versions de document. Si vous enregistrez ce document à l'aide d'Aspose.Words, le document sera enregistré sans versions.

### Exemples

Montre comment utiliser la fonction de comptage des versions des anciens documents Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// Nous pouvons lire cette propriété d'un document, mais nous ne pouvons pas la conserver lors de l'enregistrement.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");      
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


