---
title: StructuredDocumentTagCollection.GetById
second_title: Référence de l'API Aspose.Words pour .NET
description: StructuredDocumentTagCollection méthode. Renvoie la balise du document structuré par identifiant.
type: docs
weight: 30
url: /fr/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

Renvoie la balise du document structuré par identifiant.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| id | Int32 | L’identifiant de la balise du document structuré. |

### Remarques

Renvoie null si la balise de document structuré avec l'identifiant spécifié est introuvable.

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


