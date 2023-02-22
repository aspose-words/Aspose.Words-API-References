---
title: SaveOutputParameters.ContentType
second_title: Référence de l'API Aspose.Words pour .NET
description: SaveOutputParameters propriété. Renvoie la chaîne ContentType Type de média Internet qui identifie le type du document enregistré.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

Renvoie la chaîne Content-Type (Type de média Internet) qui identifie le type du document enregistré.

```csharp
public string ContentType { get; }
```

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

* class [SaveOutputParameters](../)
* espace de noms [Aspose.Words.Saving](../../saveoutputparameters/)
* Assemblée [Aspose.Words](../../../)


