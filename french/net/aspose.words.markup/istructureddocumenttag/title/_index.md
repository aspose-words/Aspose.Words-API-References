---
title: IStructuredDocumentTag.Title
second_title: Référence de l'API Aspose.Words pour .NET
description: IStructuredDocumentTag propriété. Spécifie le nom convivial associé à ce TSD . Ne peut pas être nul.
type: docs
weight: 110
url: /fr/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Spécifie le nom convivial associé à ce **TSD** . Ne peut pas être nul.

```csharp
public string Title { get; set; }
```

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

* interface [IStructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../istructureddocumenttag/)
* Assemblée [Aspose.Words](../../../)


