---
title: IStructuredDocumentTag.IsRanged
linktitle: IsRanged
articleTitle: IsRanged
second_title: Aspose.Words pour .NET
description: IStructuredDocumentTag IsRanged méthode. Renvoie vrai si cette instance est une balise de document structuré à distance en C#.
type: docs
weight: 140
url: /fr/net/aspose.words.markup/istructureddocumenttag/isranged/
---
## IStructuredDocumentTag.IsRanged method

Renvoie vrai si cette instance est une balise de document structuré à distance.

```csharp
public bool IsRanged()
```

## Exemples

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

* interface [IStructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
