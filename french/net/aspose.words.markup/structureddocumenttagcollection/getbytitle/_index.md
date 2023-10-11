---
title: StructuredDocumentTagCollection.GetByTitle
second_title: Référence de l'API Aspose.Words pour .NET
description: StructuredDocumentTagCollection méthode. Renvoie la première balise de document structuré rencontrée dans la collection avec le titre spécifié.
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

### Remarques

Renvoie null si la balise du document structuré avec le titre spécifié est introuvable.

### Exemples

Montre comment obtenir une balise de document structuré.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Récupère la balise du document structuré par Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// Récupère la balise du document structuré ou la balise à distance par titre.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Voir également

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* espace de noms [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* Assemblée [Aspose.Words](../../../)


