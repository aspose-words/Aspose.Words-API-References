---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words pour .NET
description: Convertissez facilement DocumentProperty en tableau d'octets grâce à la méthode ToByteArray. Simplifiez la gestion des données et améliorez votre efficacité de codage !
type: docs
weight: 70
url: /fr/net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

Renvoie la valeur de la propriété sous forme de tableau d'octets.

```csharp
public byte[] ToByteArray()
```

## Remarques

Lève une exception si le type de propriété n'est pasByteArray.

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

* class [DocumentProperty](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
