---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: Aspose.Words pour .NET
description: Gérez l'esthétique de vos documents avec BuiltInDocumentProperties. Obtenez ou définissez facilement des vignettes pour une présentation et une organisation optimisées.
type: docs
weight: 310
url: /fr/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Obtient ou définit la miniature du document.

```csharp
public byte[] Thumbnail { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| InvalidOperationException | Lancé si l'image n'est pas valide ou si son format n'est pas pris en charge pour un format spécifique de document. |

## Remarques

Pour l'instant, cette propriété est utilisée uniquement lorsqu'un document est exporté vers ePub, il n'est pas lu et écrit dans d'autres formats de document.

Une image de format arbitraire peut être définie sur cette propriété, mais le format est vérifié lors de l'exportation.

Seules les images gif, jpeg et png peuvent être utilisées pour la publication ePub.

## Exemples

Montre comment ajouter une vignette à un document que nous enregistrons au format Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Si nous enregistrons un document, dont la propriété « Miniature » contient des données d'image que nous avons ajoutées, en tant qu'Epub,
// un lecteur qui ouvre ce document peut afficher l'image avant la première page.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// Nous pouvons extraire l'image miniature d'un document et l'enregistrer sur le système de fichiers local.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### Voir également

* class [BuiltInDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
