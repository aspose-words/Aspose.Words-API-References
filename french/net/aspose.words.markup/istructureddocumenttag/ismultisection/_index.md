---
title: IStructuredDocumentTag.IsMultiSection
linktitle: IsMultiSection
articleTitle: IsMultiSection
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IsMultiSection de IStructuredDocumentTag, qui identifie si votre balise est une multisection à plage, améliorant ainsi l'organisation et la fonctionnalité du document.
type: docs
weight: 40
url: /fr/net/aspose.words.markup/istructureddocumenttag/ismultisection/
---
## IStructuredDocumentTag.IsMultiSection property

Renvoie vrai si cette instance est une balise de document structurée à plusieurs sections.

```csharp
public bool IsMultiSection { get; }
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
