---
title: StructuredDocumentTagCollection.RemoveAt
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTagCollection metodo. Rimuove un tag di documento strutturato nellindice specificato.
type: docs
weight: 80
url: /it/net/aspose.words.markup/structureddocumenttagcollection/removeat/
---
## StructuredDocumentTagCollection.RemoveAt method

Rimuove un tag di documento strutturato nell'indice specificato.

```csharp
public void RemoveAt(int index)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | Un indice nella raccolta. |

### Esempi

Mostra come rimuovere il tag del documento strutturato.

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
// Rimuove il tag del documento strutturato per ID.
structuredDocumentTags.Remove(1691867797);
// Rimuove il tag del documento strutturato nella posizione 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Guarda anche

* class [StructuredDocumentTagCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* assemblea [Aspose.Words](../../../)


