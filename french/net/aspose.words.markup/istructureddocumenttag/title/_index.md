---
title: IStructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Titre IStructuredDocumentTag  donnez un nom convivial à votre SDT et améliorez la clarté de votre document. En savoir plus !
type: docs
weight: 140
url: /fr/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Spécifie le nom convivial associé à ceci**SDT** . Ne peut pas être nul.

```csharp
public string Title { get; set; }
```

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

* interface [IStructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
