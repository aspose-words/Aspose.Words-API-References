---
title: Range.StructuredDocumentTags
linktitle: StructuredDocumentTags
articleTitle: StructuredDocumentTags
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Range StructuredDocumentTags, qui fournit une collection complète de balises de documents structurées, améliorant l'organisation et la fonctionnalité de votre document.
type: docs
weight: 50
url: /fr/net/aspose.words/range/structureddocumenttags/
---
## Range.StructuredDocumentTags property

Renvoie un`StructuredDocumentTags` collection qui représente toutes les balises de documents structurés dans la plage.

```csharp
public StructuredDocumentTagCollection StructuredDocumentTags { get; }
```

## Exemples

Montre comment supprimer la balise de document structuré.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

StructuredDocumentTagCollection structuredDocumentTags = doc.Range.StructuredDocumentTags;
IStructuredDocumentTag sdt;
for (int i = 0; i < structuredDocumentTags.Count; i++)
{
    sdt = structuredDocumentTags[i];
    Console.WriteLine(sdt.Title);
}

sdt = structuredDocumentTags.GetById(1691867797);
Assert.AreEqual(1691867797, sdt.Id);

Assert.AreEqual(5, structuredDocumentTags.Count);
// Supprimez la balise de document structuré par ID.
structuredDocumentTags.Remove(1691867797);
// Supprimez la balise de document structuré à la position 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Voir également

* class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* class [Range](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
