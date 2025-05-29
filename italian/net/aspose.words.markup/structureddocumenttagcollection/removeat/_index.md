---
title: StructuredDocumentTagCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words per .NET
description: Gestisci senza sforzo i tag dei tuoi documenti strutturati con il metodo RemoveAt. Rimuovi rapidamente i tag per indice per una modifica semplificata dei documenti.
type: docs
weight: 80
url: /it/net/aspose.words.markup/structureddocumenttagcollection/removeat/
---
## StructuredDocumentTagCollection.RemoveAt method

Rimuove un tag di documento strutturato all'indice specificato.

```csharp
public void RemoveAt(int index)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | Un indice della collezione. |

## Esempi

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
// Rimuovi il tag del documento strutturato tramite Id.
structuredDocumentTags.Remove(1691867797);
// Rimuovi il tag del documento strutturato dalla posizione 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Guarda anche

* class [StructuredDocumentTagCollection](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
