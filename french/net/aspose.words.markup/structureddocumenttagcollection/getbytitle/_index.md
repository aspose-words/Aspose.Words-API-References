---
title: StructuredDocumentTagCollection.GetByTitle
linktitle: GetByTitle
articleTitle: GetByTitle
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetByTitle dans StructuredDocumentTagCollection, qui récupère efficacement la première balise de document par titre pour une gestion simplifiée des données.
type: docs
weight: 50
url: /fr/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

Renvoie la première balise de document structuré rencontrée dans la collection avec le titre spécifié.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| title | String | Le titre de la balise du document structuré. |

## Remarques

Renvoie null si la balise de document structuré avec le titre spécifié est introuvable.

## Exemples

Montre comment obtenir une balise de document structurée.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Récupérez la balise du document structuré par ID.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Obtenez la balise de document structurée ou la balise à distance par titre.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Voir également

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
