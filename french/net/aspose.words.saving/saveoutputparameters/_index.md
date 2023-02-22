---
title: Class SaveOutputParameters
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.SaveOutputParameters classe. Cet objet est renvoyé à lappelant après lenregistrement dun document et contient des informations supplémentaires indiquant que a été généré ou calculé au cours de lopération denregistrement. Lappelant peut utiliser ou ignorer cet objet.
type: docs
weight: 5310
url: /fr/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Cet objet est renvoyé à l'appelant après l'enregistrement d'un document et contient des informations supplémentaires indiquant que a été généré ou calculé au cours de l'opération d'enregistrement. L'appelant peut utiliser ou ignorer cet objet.

```csharp
public class SaveOutputParameters
```

## Propriétés

| Nom | La description |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Renvoie la chaîne Content-Type (Type de média Internet) qui identifie le type du document enregistré. |

### Exemples

Montre comment accéder aux paramètres de sortie de l'opération d'enregistrement d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Après avoir enregistré un document, nous pouvons accéder au type de média Internet (type MIME) du document de sortie nouvellement créé.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Cette propriété change en fonction du format d'enregistrement.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


