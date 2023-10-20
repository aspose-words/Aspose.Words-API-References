---
title: StructuredDocumentTagCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words pour .NET
description: StructuredDocumentTagCollection Remove méthode. Supprime la balise du document structuré avec lidentifiant spécifié en C#.
type: docs
weight: 70
url: /fr/net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

Supprime la balise du document structuré avec l'identifiant spécifié.

```csharp
public void Remove(int id)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| id | Int32 | L’identifiant de la balise du document structuré. |

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
// Supprime la balise du document structuré par Id.
structuredDocumentTags.Remove(1691867797);
// Supprime la balise du document structuré à la position 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Voir également

* class [StructuredDocumentTagCollection](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
