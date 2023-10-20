---
title: SaveOutputParameters.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: Aspose.Words pour .NET
description: SaveOutputParameters ContentType propriété. Renvoie la chaîne ContentType Internet Media Type qui identifie le type du document enregistré en C#.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

Renvoie la chaîne Content-Type (Internet Media Type) qui identifie le type du document enregistré.

```csharp
public string ContentType { get; }
```

## Exemples

Montre comment accéder aux paramètres de sortie de l’opération d’enregistrement d’un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Après avoir enregistré un document, nous pouvons accéder au type de média Internet (type MIME) du document de sortie nouvellement créé.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Cette propriété change en fonction du format de sauvegarde.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Voir également

* class [SaveOutputParameters](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
