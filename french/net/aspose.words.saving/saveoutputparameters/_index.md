---
title: SaveOutputParameters Class
linktitle: SaveOutputParameters
articleTitle: SaveOutputParameters
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Saving.SaveOutputParameters, qui fournit des détails essentiels après l'enregistrement du document, améliorant ainsi votre expérience de gestion de documents.
type: docs
weight: 6390
url: /fr/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Cet objet est renvoyé à l'appelant après l'enregistrement d'un document et contient les informations supplémentaires générées ou calculées lors de l'enregistrement. L'appelant peut utiliser ou ignorer cet objet.

Pour en savoir plus, visitez le[Enregistrer un document](https://docs.aspose.com/words/net/save-a-document/) article de documentation.

```csharp
public class SaveOutputParameters
```

## Propriétés

| Nom | La description |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Renvoie la chaîne Content-Type (Internet Media Type) qui identifie le type du document enregistré. |

## Exemples

Montre comment accéder aux paramètres de sortie de l'opération d'enregistrement d'un document.

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
