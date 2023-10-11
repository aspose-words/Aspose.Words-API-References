---
title: StructuredDocumentTagCollection.RemoveAt
second_title: Référence de l'API Aspose.Words pour .NET
description: StructuredDocumentTagCollection méthode. Supprime une balise de document structuré à lindex spécifié.
type: docs
weight: 80
url: /fr/net/aspose.words.markup/structureddocumenttagcollection/removeat/
---
## StructuredDocumentTagCollection.RemoveAt method

Supprime une balise de document structuré à l'index spécifié.

```csharp
public void RemoveAt(int index)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | Un index dans la collection. |

### Exemples

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
* espace de noms [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* Assemblée [Aspose.Words](../../../)


